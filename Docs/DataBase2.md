# 18. Core Entity Specifications

---

# 18.1 Roles Table

## Purpose

Stores all system roles used for Role-Based Access Control (RBAC).

## Table

| Column | Type | Constraints | Description |
|----------|------|-------------|-------------|
| id | UUID | PK | Unique Role ID |
| name | VARCHAR(50) | UNIQUE, NOT NULL | Role Name |
| description | TEXT | NULL | Role Description |
| created_at | TIMESTAMP | NOT NULL | Creation Time |
| updated_at | TIMESTAMP | NOT NULL | Last Update |

---

### Default Roles

| Role |
|-------|
| Citizen |
| Officer |
| Department Admin |
| Super Admin |

---

### Relationships

```
Roles (1)
      │
      │
      ▼
Users (N)
```

---

# 18.2 Users Table

## Purpose

Stores authentication and profile information for every platform user.

---

| Column | Type | Constraints | Description |
|----------|------|-------------|-------------|
| id | UUID | PK |
| role_id | UUID | FK → Roles |
| first_name | VARCHAR(100) | NOT NULL |
| last_name | VARCHAR(100) | NOT NULL |
| email | VARCHAR(255) | UNIQUE |
| phone | VARCHAR(20) | UNIQUE |
| password_hash | TEXT | NOT NULL |
| profile_image | TEXT | NULL |
| language | VARCHAR(20) | DEFAULT 'en' |
| is_verified | BOOLEAN | DEFAULT FALSE |
| is_active | BOOLEAN | DEFAULT TRUE |
| last_login | TIMESTAMP | NULL |
| created_at | TIMESTAMP | NOT NULL |
| updated_at | TIMESTAMP | NOT NULL |

---

### Constraints

- Email must be unique
- Phone number must be unique
- Password stored only as bcrypt hash
- Soft delete preferred over hard delete

---

### Relationships

```
Users

↓

Complaints

↓

Notifications

↓

Audit Logs
```

---

# 18.3 Departments Table

## Purpose

Defines all municipal departments responsible for resolving complaints.

---

| Column | Type |
|----------|------|
| id | UUID |
| name | VARCHAR(150) |
| code | VARCHAR(20) |
| description | TEXT |
| email | VARCHAR(255) |
| phone | VARCHAR(20) |
| created_at | TIMESTAMP |
| updated_at | TIMESTAMP |

---

### Sample Departments

- Public Works Department
- Sanitation
- Water Supply
- Electricity
- Traffic
- Environment
- Parks & Gardens

---

### Relationships

```
Departments

↓

Officers

↓

Complaints
```

---

# 18.4 Officers Table

## Purpose

Stores municipal officers responsible for complaint resolution.

---

| Column | Type |
|----------|------|
| id | UUID |
| user_id | UUID FK |
| department_id | UUID FK |
| employee_code | VARCHAR(50) |
| designation | VARCHAR(100) |
| ward_id | UUID FK |
| status | ENUM |
| created_at | TIMESTAMP |
| updated_at | TIMESTAMP |

---

### Officer Status

- Active
- On Leave
- Busy
- Inactive

---

### Relationships

```
Department

↓

Officer

↓

Complaint Assignment
```

---

# 18.5 Wards Table

## Purpose

Represents municipal wards used for jurisdiction mapping.

---

| Column | Type |
|----------|------|
| id | UUID |
| ward_number | INTEGER |
| ward_name | VARCHAR(100) |
| polygon | geometry(POLYGON,4326) |
| created_at | TIMESTAMP |

---

### Why Polygon?

Each ward represents an administrative boundary.

Using PostGIS polygon enables:

- Automatic ward detection
- Officer assignment
- Heatmaps
- Analytics
- Area calculations

---

# 18.6 Locations Table

## Purpose

Stores precise geographical coordinates.

---

| Column | Type |
|----------|------|
| id | UUID |
| address | TEXT |
| city | VARCHAR(100) |
| district | VARCHAR(100) |
| state | VARCHAR(100) |
| pincode | VARCHAR(10) |
| geometry | geometry(Point,4326) |
| ward_id | UUID FK |
| created_at | TIMESTAMP |

---

### Why Separate Locations?

Many entities can reuse locations:

- Complaints
- Departments
- Officers
- Future IoT Devices

Avoids duplication.

---

### Spatial Index

```sql
CREATE INDEX idx_location_geom
ON locations
USING GIST (geometry);
```

---

# 18.7 Complaints Table

## Purpose

Central entity of the platform.

Stores citizen complaints.

---

| Column | Type |
|----------|------|
| id | UUID |
| complaint_number | VARCHAR(30) UNIQUE |
| citizen_id | UUID FK |
| department_id | UUID FK |
| location_id | UUID FK |
| title | VARCHAR(255) |
| description | TEXT |
| category | VARCHAR(100) |
| priority | VARCHAR(50) |
| status | VARCHAR(50) |
| source | VARCHAR(50) |
| submitted_at | TIMESTAMP |
| resolved_at | TIMESTAMP |
| created_at | TIMESTAMP |
| updated_at | TIMESTAMP |

---

### Complaint Status

- Submitted
- Under Review
- Assigned
- In Progress
- Resolved
- Rejected
- Closed

---

### Complaint Priority

- Low
- Medium
- High
- Critical

---

### Complaint Source

- Mobile App
- Dashboard
- API
- WhatsApp (Future)
- IoT Device (Future)

---

### Relationships

```
Citizen

↓

Complaint

↓

Images

↓

AI Analysis

↓

Assignments

↓

History

↓

Notifications
```

---

# Complaint Lifecycle

```text
Citizen

↓

Complaint Created

↓

AI Analysis

↓

Department Assigned

↓

Officer Assigned

↓

Work Started

↓

Resolved

↓

Citizen Feedback

↓

Closed
```

---

# Entity Summary

| Entity | Responsibility |
|----------|----------------|
| Roles | RBAC |
| Users | Authentication |
| Departments | Municipal Units |
| Officers | Complaint Resolution |
| Wards | Jurisdiction |
| Locations | GIS |
| Complaints | Core Business Entity |

---

# Design Decisions

## Why Separate Officers & Users?

Every officer is a user.

But every user is **not** an officer.

This keeps authentication independent from organizational structure.

---

## Why Separate Locations?

Eliminates duplicate address storage.

Supports:

- GIS
- Reverse Geocoding
- Heatmaps
- Future Asset Tracking

---

## Why UUID Everywhere?

- Secure IDs
- Offline creation
- Future microservices
- Easier synchronization

---

# Next Section

DATABASE.md Part 3 covers:

- Complaint Images
- Complaint History
- Complaint Comments
- AI Analysis
- Duplicate Detection
- Notifications
- Audit Logs
- Refresh Tokens
- Sessions
- Image Metadata
