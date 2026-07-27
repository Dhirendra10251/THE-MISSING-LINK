# 📚 DECISIONS.md

> Architecture Decision Records (ADR)

Every major technical decision must be recorded here.

---

# ADR-001

## Decision

Use NestJS instead of Express.js.

### Reason

- Modular architecture
- Dependency Injection
- Enterprise-ready
- Built-in validation
- Better scalability

### Alternatives

Express.js

Fastify

### Status

Accepted

---

# ADR-002

## Decision

Use PostgreSQL + PostGIS.

### Reason

- Spatial queries
- GIS support
- ACID compliance
- Better relational modelling

### Alternatives

MongoDB

MySQL

### Status

Accepted

---

# ADR-003

## Decision

Separate AI into a FastAPI microservice.

### Reason

- Python AI ecosystem
- Easier Gemini integration
- Independent scaling
- Cleaner architecture

### Alternatives

Node AI libraries

Monolithic backend

### Status

Accepted

---

# ADR-004

## Decision

Use Google Gemini via Google AI Studio.

### Reason

- Sponsor alignment
- Vision capabilities
- Function Calling
- Summarization
- Multimodal support

### Alternatives

OpenAI

Claude

Llama

### Status

Accepted

---

# ADR-005

## Decision

Citizen application will use Flutter.

### Reason

- Single codebase
- Faster development
- Native performance
- Android-first deployment

### Status

Accepted

---

# ADR-006

## Decision

Admin Dashboard will use Next.js.

### Reason

- React ecosystem
- SEO support
- Component reuse
- Performance

### Status

Accepted

---

# ADR-007

## Decision

Use Cloudinary for media storage.

### Reason

- Optimized image delivery
- Easy uploads
- Free tier
- CDN support

### Status

Accepted

---

# ADR-008

## Decision

Follow Modular Monolith architecture for MVP.

### Reason

- Faster development
- Easier debugging
- Hackathon friendly
- Can evolve into microservices later

### Status

Accepted

---

# ADR-009

## Decision

Target only a 30–40% functional prototype.

### Reason

- Required by SVH Round 1
- Prioritize architecture over feature quantity
- Deliver polished core functionality

### Status

Accepted

---

# ADR-010

## Decision

Prioritize AI-assisted governance over feature count.

### Reason

Winning criteria emphasize:

- Innovation
- Technical approach
- Practical feasibility

AI-driven automation provides a stronger Unique Value Proposition than adding numerous CRUD features.

### Status

Accepted
