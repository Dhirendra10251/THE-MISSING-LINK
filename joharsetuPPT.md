# JoharSetu — SVH 2026 Slide Content (6-slide template)

Everything below is written as slide-ready bullets, matched exactly to your official template's section headings. Paste directly into the provided .pptx template — don't rebuild the template itself, just fill it. Anything in [brackets] is a placeholder you need to confirm or insert yourself — flagged explicitly below rather than guessed.

---

## SLIDE 1 — TITLE PAGE

- **Problem Statement ID:** SVH26005
- **Problem Statement Title:** [Confirm exact wording against your official SVH26005 statement — reconstructed here as: "Crowdsourced Civic Issue Reporting & Priority Escalation System for Urban Local Bodies." Don't submit this without checking it against the literal text on the SVH portal — portals often auto-validate this field.]
- **Theme:** Clean & Green Technology
- **PS Category:** Software
- **Team ID:** [Insert your registered Team ID]
- **Team Name:** [Insert your registered Team Name]

---

## SLIDE 2 — IDEA TITLE

**Idea Title:** JoharSetu (जोहार सेतु) — A Bridge Between Citizen and Administration

### Proposed Solution (Describe your Idea/Solution/Prototype)
- A crowdsourced civic-issue reporting platform for Jharkhand's Urban Local Bodies (ULBs) — citizens report potholes, open drains, overflowing bins, streetlight outages, and illegal dumping with photo + GPS, no login required.
- Duplicate reports of the same issue corroborate one ticket instead of creating noise — priority score rises automatically with each corroboration, category severity, and SLA proximity.
- Departments cannot self-certify a ticket "Resolved" — a field worker must submit a geofenced, photo-verified before/after proof; the original citizen then confirms or disputes the fix.
- A public Ward Green Score dashboard ranks municipal wards by resolved-vs-open ratio, creating transparency and inter-ward accountability.

### How it addresses the problem
- India's national grievance system (CPGRAMS) treats every complaint as an independent case, with no duplicate detection and no independent field verification of closure.
- Jharkhand's own recent civic survey data shows a real citizen-participation gap — several ULBs recorded feedback from fewer than 10 citizens — which JoharSetu's zero-friction anonymous reporting and Eco Points are built directly against.

### Innovation and uniqueness of the solution
- Corroboration-as-signal instead of duplicate-as-noise.
- Geofenced photo-proof resolution — closes the "self-certified closure" trust gap that generic grievance portals leave open.
- Built and styled as an authentic, accessible ULB-grade government portal (GIGW-inspired UI, screen-reader and font-scaling controls, Google Translate) rather than a generic ticket tracker.

---

## SLIDE 3 — TECHNICAL APPROACH

### Technologies to be used
- Frontend: React + Vite, installable as a Progressive Web App
- Backend: Firebase — Firestore, Cloud Functions, Storage, Auth
- Maps: Leaflet.js + OpenStreetMap with geohash-based proximity clustering
- Accessibility/Localization: Google Website Translator widget, screen-reader and font-scaling controls

### Methodology and process for implementation
- [Insert the ticket lifecycle flowchart here: Submit → Corroborate → Auto-Prioritize → Assign → Field Verify (photo proof) → Citizen Confirms/Disputes — say the word if you want it regenerated in a size that fits this exact slide.]
- Priority score = weighted function of severity, corroboration count, category weight, time decay, vulnerable-zone proximity, and SLA breach status
- [Insert 1–2 working-prototype screenshots here: public map dashboard + admin priority queue, to satisfy the "working prototype" requirement directly on this slide]

---

## SLIDE 4 — FEASIBILITY AND VIABILITY

### Analysis of the feasibility of the idea
- Built entirely on serverless, free-tier-friendly infrastructure (Firebase) — deployable across ULBs without new hardware or heavy backend operations.
- Aligns with existing national digital-literacy infrastructure, which lowers onboarding friction for both citizens and municipal staff.

### Potential challenges and risks
- Jharkhand's internet penetration trails the national leaders, especially in rural and tribal blocks.
- Indoor or dense-forest GPS accuracy could affect geofenced field-verification checks.
- Jharkhand's Urban Local Bodies each run independently — staff adoption resistance across many separate departments is a real risk.
- Historically low citizen participation in some ULBs' official feedback processes.

### Strategies for overcoming these challenges
- PWA offline queue with background sync for low-connectivity users.
- Manual override on geofence checks — human-in-loop, not a fully automated block.
- Phased pilot rollout starting with one or two ULBs before statewide scaling, rather than a single big-bang launch.
- Eco Points and zero-login guest reporting specifically targeted at closing the documented participation gap.

---

## SLIDE 5 — IMPACT AND BENEFITS

### Potential impact on the target audience
- Direct reach across Jharkhand's Urban Local Bodies — over 43 lakh registered ULB voters as a rough proxy for the reachable adult urban population.
- Targets a specific, documented gap: several ULBs recorded civic feedback from fewer than 10 citizens in the state's own recent survey.

### Benefits of the solution (social, economic, environmental, etc.)
- **Social:** faster resolution of hazard-level issues (e.g. open drains near schools) through SLA-driven prioritization tighter than blanket national timelines.
- **Economic:** fewer redundant field visits caused by duplicate complaints, more efficient routing of limited municipal field staff.
- **Environmental:** directly supports the Clean & Green Technology theme and each ULB's cleanliness-ranking performance.
- **Governance:** Ward Green Score creates public accountability and inter-ward competition — the same competitive mechanic that has already driven real improvement in state cleanliness rankings.

---

## SLIDE 6 — RESEARCH AND REFERENCES

- List of Urban Local Bodies in Jharkhand — Wikipedia / Jharkhand State Election Commission, 2026
- Jharkhand E-Governance & SUDA — jharkhandegovernance.com
- CPGRAMS (Centralised Public Grievance Redress and Monitoring System) — pgportal.gov.in; DARPG order reducing the statutory redressal timeline to 21 days, August 2024
- Swachh Survekshan 2024–25 results and citizen-feedback participation data — PIB; The Statesman; Jharkhand Mirror; Avenue Mail
- "Internet in India 2024" report — Kantar / Internet and Mobile Association of India (IAMAI), state-wise internet penetration
- Jharkhand Municipal Act, 2011

---

**Reminder from your own template (slide 7 of the source file): delete the "Important Instructions" slide before uploading, and the whole deck must be exported and submitted as a PDF — no .pptx or .docx accepted.**
