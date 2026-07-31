# UrjaSetu — Content to Fill Into the Official SVH Template

⚠️ **Read this first:**
- Total slides after you're done: **6** (title slide included). Do not add extra slides.
- Fill content **under the exact bullet stems already in the template** — don't rename or remove them.
- Final file must be exported and uploaded as **PDF only**.
- **Delete the "Important Instructions" slide** before you export/upload.

---

## Slide 1 — Title Page

- Problem Statement ID: **SVH26004**
- Problem Statement Title: **Hybrid Renewable Energy Generation Solution**
- Theme: **Clean & Green Technology**
- PS Category: **Software**
- Team ID: *[fill in]*
- Team Name (registered on portal): *[fill in]*
- (Optional, doesn't remove anything required) Solution name: **UrjaSetu**

---

## Slide 2 — Idea Title ("UrjaSetu") / Proposed Solution

**Detailed explanation of the proposed solution**
- UrjaSetu is a vendor-neutral software layer that unifies a campus's solar, wind, battery and grid connection into one coordinated Virtual Power Plant (VPP).
- Forecasts generation and demand, issues real-time recommendations for battery charge/discharge, load-shifting, and export/curtailment.

**How it addresses the problem**
- Solves the "orchestration, not procurement" gap called out in the problem statement — existing assets run in isolation; UrjaSetu adds the missing coordination layer.
- Zero new hardware — plugs into existing meters/inverters through a protocol adapter.

**Innovation and uniqueness of the solution**
- Vendor-neutral adapter — works with any inverter/turbine/battery brand.
- Explainable, plain-language recommendations — no specialized staff training needed.
- Built for statewide scale from day one — single-campus view + DTE-wide aggregate view.
- Maps directly onto Rajasthan's 2025 RERC Virtual/Group Net Metering regulations — a real, current policy pathway, not just a technical idea.

---

## Slide 3 — Technical Approach

**Technologies to be used**
- React (frontend) · FastAPI (backend) · PostgreSQL/TimescaleDB (time-series data) · Prophet/ML forecasting · Modbus/MQTT adapters · Open-Meteo weather API

**Methodology and process for implementation (Flow Charts/Images/working prototype)**
- *[Insert architecture diagram screenshot here]*
- *[Insert dashboard mockup screenshot here]*
- *[Insert what-if simulator screenshot here]*
- Flow: Hardware inputs → adapter layer → data store → forecasting + digital twin → optimization engine → recommendations dashboard

**Product status**
- Early-stage prototype (~30–35% complete): architecture validated, UI/UX mockups built and functional as demos; forecasting and optimization logic in active design.

---

## Slide 4 — Feasibility and Viability

**Analysis of the feasibility of the idea**
- Software-only deployment on existing meters/inverters — no new hardware cost.
- Directly aligned with RERC's 2025 Virtual/Group Net Metering regulations — a real regulatory mechanism already exists for this exact model.

**Potential challenges and risks**
- Forecast accuracy during monsoon/heavy cloud cover.
- Connectivity gaps at rural campuses.
- Diversity of vendor hardware protocols.

**Strategies for overcoming these challenges**
- Confidence-interval based conservative fallback recommendations.
- Local edge caching for offline operation.
- Vendor-neutral adapter layer (Modbus/MQTT/OPC-UA) built as a core design principle, not an afterthought.

---

## Slide 5 — Impact and Benefits

**Potential impact on the target audience**
- Public-sector campuses across Rajasthan under DTE — facility staff, students, hostels, and labs.

**Benefits of the solution (social, economic, environmental)**
- Renewable self-consumption: ~55–65% (uncoordinated) → ~75–85% (coordinated) — illustrative estimate, to be validated with pilot data.
- Direct ₹ savings and measurable CO₂ reduction.
- Zero specialized training — usable immediately by non-technical staff.
- Scalable statewide — one platform, every DTE campus.

---

## Slide 6 — Research and References

- RERC Third Amendment Regulations, 2025 — Virtual & Group Net Metering
- Rajasthan Integrated Clean Energy Policy, 2024
- *[Add 1–2 direct links your research helper found]*

---

## Before You Upload — Final Checklist
- [ ] Exactly 6 slides remain
- [ ] "Important Instructions" slide deleted
- [ ] No paragraphs — points, diagrams, and screenshots only
- [ ] All three mockup screenshots inserted into Slide 3
- [ ] File exported and saved as **PDF**
- [ ] Team ID / Team Name filled in on Slide 1
