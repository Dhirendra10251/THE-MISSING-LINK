# 🏗️ ARCHITECTURE.md

# NagrikSeva Architecture Documentation

> **Version:** 1.0
> **Architecture Style:** Modular Monolith (MVP) → Microservice Ready
> **Project:** NagrikSeva – AI-Powered Civic Intelligence Platform
> **Status:** Architecture Approved

---

# 1. Architecture Philosophy

NagrikSeva is designed as an **AI-first Civic Intelligence Platform**, not merely a complaint management system.

The architecture prioritizes:

- Separation of Concerns
- Scalability
- Security
- AI-assisted automation
- Geospatial intelligence
- Production readiness
- Future microservice migration

For the MVP (30–40%), a **Modular Monolith** architecture is chosen to maximize development speed while preserving clean module boundaries. This allows seamless migration to independent microservices in later phases.

---

# 2. High-Level System Architecture

```text
                   +----------------------+
                   |   Citizen Mobile App |
                   |      (Flutter)       |
                   +----------+-----------+
                              |
                     HTTPS REST APIs
                              |
                              ▼
                 +--------------------------+
                 |     API Gateway          |
                 |        (NestJS)          |
                 +------------+-------------+
                              |
        -----------------------------------------------------
        |            |              |            |           |
        ▼            ▼              ▼            ▼           ▼
 Authentication  Complaint      User        Notification   Analytics
    Module         Module      Module         Module        Module
        |            |              |            |           |
        -----------------------------
                     |
                     ▼
          PostgreSQL + PostGIS
                     |
             Redis Cache Layer
                     |
                     ▼
          AI Orchestrator Service
                     |
                     ▼
          FastAPI AI Microservice
                     |
      -----------------------------------------
      |          |          |        |         |
      ▼          ▼          ▼        ▼         ▼
 Gemini AI   OCR Engine   EXIF   Embeddings  Duplicate
                          Parser              Detection
                     |
                     ▼
         Cloudinary Image Storage
                     |
                     ▼
          Admin Command Dashboard
              (Next.js + React)
```

---

# 3. C4 Context Diagram

```text
                    Citizens
                       │
                       ▼
               Flutter Mobile App
                       │
                       ▼
                  NagrikSeva
                       │
      ┌────────────────┼──────────────────┐
      ▼                ▼                  ▼
 Google Maps      Cloudinary         Google Gemini
      │                │                  │
      ▼                ▼                  ▼
   Location         Image Store      AI Services
```

---

# 4. Component Architecture

## Citizen App

Responsibilities:

- Login
- Register
- Report Complaint
- Camera
- Maps
- Complaint Tracking
- Notifications
- Profile

---

## Backend

Responsibilities:

- Authentication
- Complaint Management
- Officer Assignment
- API Validation
- Notifications
- AI Orchestration
- Analytics

---

## AI Service

Responsibilities:

- Complaint Classification
- Duplicate Detection
- Severity Prediction
- Department Recommendation
- Image Validation
- Summarization

---

## Dashboard

Responsibilities:

- Officer Dashboard
- Complaint Monitoring
- GIS Maps
- Analytics
- Reports
- Heatmaps

---

# 5. Backend Module Diagram

```text
NestJS

├── Auth Module
├── User Module
├── Complaint Module
├── Officer Module
├── Department Module
├── Notification Module
├── Analytics Module
├── AI Gateway Module
├── File Upload Module
├── Maps Module
└── Shared Module
```

---

# 6. AI Pipeline

```text
Citizen Uploads Image

        │

        ▼

Image Validation

        │

        ▼

EXIF Extraction

        │

        ▼

GPS Validation

        │

        ▼

Gemini Vision Analysis

        │

        ▼

Category Prediction

        │

        ▼

Severity Prediction

        │

        ▼

Department Recommendation

        │

        ▼

Duplicate Detection

        │

        ▼

Store Results

        │

        ▼

Officer Dashboard
```

---

# 7. Complaint Lifecycle

```text
Citizen

↓

Create Complaint

↓

Image Upload

↓

GPS Captured

↓

Backend Validation

↓

AI Analysis

↓

Department Assignment

↓

Officer Receives Complaint

↓

Status Updated

↓

Citizen Notified

↓

Complaint Closed
```

---

# 8. Sequence Diagram

```text
Citizen

│

│ Submit Complaint

▼

Flutter App

│

│ REST API

▼

NestJS

│

│ Save Complaint

▼

PostgreSQL

│

│ Request AI Analysis

▼

FastAPI

│

│ Gemini

▼

AI Response

│

▼

NestJS

│

▼

Officer Dashboard

│

▼

Citizen Notification
```

---

# 9. Database Architecture

Core Entities

- Users
- Roles
- Complaints
- Departments
- Officers
- Complaint Images
- Complaint History
- Notifications
- AI Analysis
- Ward
- Location

Relationships

User

↓

Complaint

↓

Complaint Image

↓

AI Analysis

↓

Officer

↓

Department

↓

Status History

---

# 10. Security Architecture

Authentication

JWT

Authorization

RBAC

Encryption

HTTPS

Password Hashing

bcrypt

Uploads

Cloudinary

Validation

DTO + class-validator

Rate Limiting

NestJS Throttler

---

# 11. AI Decision Flow

```text
Image

↓

Gemini Vision

↓

Category

↓

Severity

↓

Department

↓

Duplicate Check

↓

Recommendation

↓

Store JSON

↓

Dashboard
```

---

# 12. Deployment Architecture

```text
Flutter

↓

Google Play

↓

NestJS

↓

Docker

↓

Railway / Cloud Run

↓

PostgreSQL

↓

Cloudinary

↓

Gemini API

↓

Dashboard
```

---

# 13. Scalability Strategy

Current

Modular Monolith

↓

Future

Complaint Service

↓

AI Service

↓

Notification Service

↓

Analytics Service

↓

API Gateway

↓

Kubernetes

---

# 14. Performance Goals

API

<300 ms

Authentication

<200 ms

Dashboard

<2 sec

AI

<5 sec

Maps

60 FPS

Image Upload

<3 sec

---

# 15. Fault Tolerance

AI Failure

↓

Fallback Rules

↓

Manual Department Selection

↓

Complaint Still Accepted

Image Failure

↓

Retry Upload

↓

Notify User

Notification Failure

↓

Retry Queue

↓

Email Backup

---

# 16. Logging Strategy

Authentication

Complaint Creation

AI Requests

Officer Updates

Errors

System Health

Audit Trail

---

# 17. Monitoring

Future Integration

Google Cloud Monitoring

Grafana

Prometheus

Sentry

---

# 18. Future Architecture

- IoT Sensor Integration
- Drone Inspection APIs
- Smart CCTV Integration
- WhatsApp Bot
- Voice Assistant
- Predictive Infrastructure Analytics
- Multi-State Deployment
- Multi-Tenant Architecture

---

# 19. Design Principles

- SOLID Principles
- Clean Architecture
- DRY
- KISS
- Separation of Concerns
- Event-Driven Thinking
- API-First Development
- AI-Assisted Decision Support

---

# 20. Architecture Status

| Component | Status |
|------------|--------|
| System Architecture | ✅ Approved |
| Technology Stack | ✅ Approved |
| AI Architecture | ✅ Approved |
| Security Model | ✅ Approved |
| Deployment Strategy | ✅ Approved |
| Scalability Strategy | ✅ Approved |

---

## Version History

| Version | Date | Changes |
|----------|------|----------|
| 1.0 | July 2026 | Initial architecture approved |
