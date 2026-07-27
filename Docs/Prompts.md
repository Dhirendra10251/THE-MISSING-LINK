# 🧠 PROMPTS.md

> Reusable prompt templates for Claude Sonnet 5.
>
> These prompts ensure consistency across all development sessions while minimizing context usage.

---

# Global Context Prompt

Use this at the beginning of every new Claude chat.

```text
You are the Lead Software Architect for the NagrikSeva project.

Before responding:

1. Treat PROJECT.md as the source of truth.
2. Follow every rule in RULES.md.
3. Maintain architectural consistency.
4. Never contradict previous decisions in DECISIONS.md.
5. Keep scalability, maintainability, and hackathon feasibility in mind.

If you need assumptions, explicitly state them before implementation.
```

---

# Module Development Prompt

```text
Task:
Build the following module:

<Module Name>

Requirements:

Follow PROJECT.md

Follow RULES.md

Do not modify unrelated modules

Generate production-ready code

Explain major design decisions briefly

Include folder structure changes

Include integration notes

Stop after this module

Output:

Architecture

Folder Structure

Implementation

Testing Notes

Next Module
```

---

# Code Review Prompt

```text
Act as a Staff Software Engineer.

Review the supplied code for:

Architecture violations

Security issues

Performance problems

SOLID principles

Maintainability

Scalability

Return improvements in priority order.

Do not rewrite unless necessary.
```

---

# Bug Fix Prompt

```text
Analyze the following bug.

Identify:

Root Cause

Impact

Fix

Potential side effects

Regression risks

Provide only the required code modifications.
```

---

# Refactoring Prompt

```text
Refactor the supplied module without changing functionality.

Goals:

Cleaner architecture

Reduced complexity

Improved readability

Better performance

No breaking changes
```

---

# Documentation Prompt

```text
Generate technical documentation for the supplied module.

Include:

Purpose

Architecture

Dependencies

API Endpoints

Database interactions

Error handling

Future improvements
```

---

# API Design Prompt

```text
Design production-ready REST APIs for:

<Feature>

Include:

Routes

Request DTOs

Response DTOs

Validation

Status Codes

Error Responses

Authentication

Swagger examples
```

---

# AI Feature Prompt

```text
Design the AI workflow for:

<Feature>

Include:

Input

Prompt Engineering

Gemini Usage

Expected JSON Output

Confidence Score

Failure Handling

Integration with Backend
```

---

# Flutter Screen Prompt

```text
Develop the Flutter screen:

<Screen Name>

Requirements:

Responsive UI

Reusable widgets

Riverpod/BLoC compatible

API integration ready

Validation

Loading/Error states

Navigation support
```

---

# Dashboard Prompt

```text
Develop the Admin Dashboard module.

Requirements:

Next.js

React

TailwindCSS

Charts

Maps

Responsive

Role-based access

Clean architecture

Only build this module.
```

---

# Deployment Prompt

```text
Prepare the deployment environment.

Include:

Docker

Docker Compose

Environment Variables

GitHub Actions

Cloud Run / Railway

Production configuration

Security Checklist
```

---

# Presentation Prompt

```text
Convert the completed module into hackathon presentation content.

Include:

Problem solved

Innovation

Technical depth

Architecture

Demo highlights

Judge talking points

Maximum one slide.
```

---

# Demo Prompt

```text
Create a live demo walkthrough.

For each feature provide:

User action

System processing

Expected output

Judge takeaway

Total duration under 5 minutes.
```
