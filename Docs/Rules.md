# 📜 RULES.md
# NagrikSeva Engineering & Development Standards

> **Purpose**
>
> This document defines the permanent engineering, architecture, coding, AI, documentation, and development standards for the NagrikSeva project.
>
> Every implementation must strictly follow these rules unless explicitly overridden.

---

# 1. Core Philosophy

NagrikSeva is **NOT** a simple complaint management application.

It is an **AI-powered Civic Intelligence Platform**.

Every feature should answer one of these questions:

- Does this reduce government workload?
- Does this improve citizen experience?
- Does AI automate manual work?
- Does this improve transparency?
- Does this help city-wide planning?

If the answer is "No", reconsider the feature.

---

# 2. Project Priorities

Priority order:

1. Problem-Solution Alignment
2. Innovation
3. Technical Feasibility
4. Scalability
5. Clean UI/UX
6. Code Quality

Never sacrifice the first four priorities for unnecessary features.

---

# 3. Architecture Rules

The project follows a modular service-oriented architecture.

Citizen App
↓

API Gateway

↓

NestJS Backend

↓

PostgreSQL + PostGIS

↓

FastAPI AI Service

↓

Admin Dashboard

Rules

- Backend must never contain AI inference logic.
- AI must run only inside the FastAPI service.
- Frontend never accesses the database directly.
- Business logic belongs inside backend services.
- Database access is centralized.
- Services must remain loosely coupled.

---

# 4. Technology Standards

Citizen App

Flutter

Admin Dashboard

Next.js

React

TailwindCSS

ShadCN UI

Backend

NestJS

TypeScript

REST APIs

Swagger

Validation

AI

FastAPI

Python

Google Gemini

Google AI Studio

OCR

Embeddings

Image Similarity

Database

PostgreSQL

PostGIS

Redis

Storage

Cloudinary

Maps

Google Maps Platform

---

# 5. Coding Standards

Use

TypeScript (Backend)

Python (AI)

Dart (Flutter)

Mandatory

Meaningful variable names

Small functions

Single Responsibility Principle

Dependency Injection

Reusable components

No duplicate code

No magic numbers

No hardcoded secrets

Every module must compile independently.

---

# 6. Folder Structure

Never violate the agreed project structure.

backend/

frontend/

admin/

ai/

docs/

docker/

.github/

Each module owns its responsibilities.

---

# 7. API Standards

RESTful naming only.

Good

GET /complaints

POST /complaints

PATCH /complaints/:id

Bad

/getComplaint

/updateComplaint

/deleteComplaint

Use

HTTP Status Codes

DTOs

Validation

Version APIs if necessary.

---

# 8. Database Rules

Always normalize data.

Use

UUID primary keys

Foreign Keys

Indexes

Transactions

PostGIS geometry types

Avoid

Duplicate columns

Business logic in SQL

Unnecessary joins

---

# 9. Authentication

JWT Authentication

RBAC

Roles

Citizen

Officer

Department Admin

Super Admin

Never expose protected endpoints without authorization.

---

# 10. AI Rules

AI must always assist humans.

Never replace human decisions completely.

AI outputs should include

Confidence Score

Reason

Recommendation

Example

Severity

High

Confidence

92%

Reason

Road obstruction covering both lanes.

---

# 11. AI Prompt Engineering

Every prompt should

Define role

Define context

Specify expected output

Return structured JSON

Avoid vague prompts.

---

# 12. Google AI Studio Usage

Maximize usage.

Use Gemini for

Vision

Classification

Summarization

Natural Language Search

Department Routing

Function Calling

Prompt Chaining

Semantic Analysis

Mention Google AI wherever appropriate in documentation and presentation.

---

# 13. Image Processing Rules

Every uploaded image should undergo

EXIF extraction

GPS validation

Compression

Image quality verification

Duplicate detection

AI classification

No image should bypass validation.

---

# 14. Error Handling

Never expose stack traces.

Return

Error Code

Message

Timestamp

Request ID

Always log unexpected exceptions.

---

# 15. Logging

Use structured logs.

Log

Authentication

Complaint creation

AI processing

Status changes

Officer assignment

Avoid logging sensitive user data.

---

# 16. Security

Mandatory

Input validation

Rate limiting

JWT

HTTPS

Secure file uploads

CORS

Helmet

Sanitize user inputs

Never trust frontend validation.

---

# 17. Performance

API response

<300 ms

Dashboard load

<2 seconds

Map rendering

Smooth

Image upload

Compressed before storage

AI requests should execute asynchronously whenever possible.

---

# 18. UI/UX Rules

Citizen interface

Minimal

Simple

Accessible

One-handed usage

Dashboard

Data-first

Charts

Maps

Heatmaps

Minimal clicks

Responsive layouts only.

---

# 19. Git Rules

Branch naming

feature/auth

feature/dashboard

feature/ai

bugfix/maps

Commits

feat:

fix:

docs:

refactor:

test:

chore:

Never commit generated files.

---

# 20. Documentation Rules

Every module must include

Purpose

Dependencies

Architecture

API references

Environment variables

Future improvements

Documentation is mandatory.

---

# 21. Testing Standards

Backend

Unit tests

Integration tests

Flutter

Widget tests

AI

Sample inference tests

Never merge completely untested modules.

---

# 22. Presentation Rules

Every implemented feature should strengthen at least one judging criterion.

✓ Innovation

✓ Feasibility

✓ Scalability

✓ Technical depth

Avoid adding features that cannot be demonstrated.

---

# 23. Demo Rules

Every feature must have

Input

Processing

Visible output

Judges should understand each feature in less than 30 seconds.

---

# 24. Prototype Scope

Round 1 prototype target:

30–40% implementation.

Focus on

Authentication

Complaint Reporting

Maps

Image Upload

AI Categorization

Dashboard

Do NOT spend time implementing enterprise-scale features that cannot be demonstrated.

---

# 25. Definition of Done

A module is complete only if it includes

✓ Production-quality code

✓ Validation

✓ Error handling

✓ Documentation

✓ Responsive UI (if applicable)

✓ Testing (basic)

✓ Git-ready structure

✓ Integration notes

---

# 26. Claude Development Workflow

Claude must follow this sequence for every request:

1. Analyze the task
2. Explain the design
3. Generate the implementation
4. Explain integration
5. List assumptions
6. Suggest the next module

Never generate unrelated modules.

---

# 27. Absolute Rules

Never break architecture.

Never duplicate code.

Never hardcode secrets.

Never ignore documentation.

Never sacrifice maintainability for speed.

Always optimize for hackathon judging criteria.

Always think like a Senior Software Architect.
