# UrjaSetu — 4-Day Sprint to Submission (Aug 1 → Aug 5)

## Reality Check First — Read This Out Loud to Your Team

**Only the PPT is due on Aug 5. No working prototype, no code, no demo.** This is genuinely good news:
- Your "vibe code only" tech guy does **not** need to build a functioning backend, database, or ML model in 4 days. Trying to do that would burn your only technical person on something that isn't even being judged.
- The entire team's energy should go into **one thing**: a sharp, credible, visually convincing idea presentation that nails the six things judges score (Novelty, Complexity, Clarity, Feasibility, Practicability, Sustainability — see the main ideation doc, §11).
- "Credible" does not mean "working code." It means: clear diagrams, a confident narrative, real numbers/policy references, and a couple of good-looking mockup visuals. That's 100% achievable in 4 days with this team.

---

## Role Assignment — Matched to Your Actual Team, Not an Ideal Team

Don't fight your team's real dynamics. Assign around them.

| Person | Job (and ONLY this job) |
|---|---|
| **Tech guy** | Produce 2–3 **visual assets** for the deck: (1) a clean architecture diagram, (2) a dashboard/UI mockup screenshot (can be built fast with an AI app builder — v0.dev, bolt.new, Claude, or even Figma AI — it doesn't need to actually work, it just needs to look real), (3) optionally, one "what-if simulator" mockup screenshot. That's it. No backend, no database, no real forecasting model. |
| **PPT person 1 — Content Writer** | Owns the *words* on every slide: problem framing, solution narrative, feasibility argument, impact numbers. Pulls directly from the ideation doc (previous file) and the slide-by-slide draft below. |
| **PPT person 2 — Slide Designer** | Owns the *look*: consistent template, fonts, colors, inserting the tech guy's visuals in the right spots, making sure it matches your SPOC's required format exactly. |
| **Pitch person** | Owns the script, timing, and delivery. Reads the full ideation doc + the Judges' Q&A section (§16 of the main doc) cold. Rehearses out loud, not just silently reading. |
| **Helping hand 1** | Research support: pull 3–4 real numbers/facts to strengthen credibility (Rajasthan solar irradiance stats, RERC net-metering figures, any public data on campus energy use). Also handles logistics — confirm exact submission format, file size limit, naming convention, and portal deadline (submit early, not at the last minute). |
| **Helping hand 2** | Proofreading, formatting consistency check, timer/stopwatch during rehearsals, and sourcing clean non-copyrighted icons/images if the deck needs them. |

This spreads real, doable work to all 6 people — including the two who "just help" — without requiring skills they don't have.

---

## Day-by-Day Plan

### Day 1 — Today (Aug 1)
- **Whole team, 30 min:** align on the one-liner and lock the name (**UrjaSetu**). Everyone should be able to repeat the elevator pitch from memory by end of this call.
- **Tech guy:** start the architecture diagram + begin the dashboard mockup.
- **Content Writer:** draft slides 1–5 (title, problem, idea, architecture placeholder, USPs) using the content below.
- **Pitch person:** read the full ideation doc once, start drafting the opening hook + closing line.
- **Helping hand 1:** pull the 3–4 supporting numbers/facts now, so writers aren't blocked later.
- **Helping hand 2:** confirm submission format/deadline/portal with the SPOC today — don't leave this until Aug 4.

### Day 2 (Aug 2)
- **Tech guy:** finish and export both mockup visuals as clean images.
- **Content Writer:** draft slides 6–10 (feasibility, impact numbers, tech stack, scalability, team/references).
- **Slide Designer:** start assembling deck v1, dropping in visuals as they arrive.
- **Pitch person:** do a rough run-through against deck v1 draft, flag any slide that's confusing or too text-heavy.

### Day 3 (Aug 3)
- **Full team:** first complete draft exists — group review session. Specifically check every slide against the problem statement's own language: does it clearly show *orchestration not procurement*, *vendor-neutral*, and *no specialized training required*? If a slide doesn't reinforce at least one of these, tighten it.
- **Tech guy:** polish visuals based on feedback; add a simple before/after self-consumption comparison chart if time allows.
- **Pitch person:** full timed rehearsal + Q&A stress test (other team members fire questions from the Q&A prep list).

### Day 4 (Aug 4)
- **Final polish only.** Typos, alignment, consistent fonts/colors, exact SPOC template compliance.
- **Two full rehearsals minimum**, out loud, with a timer.
- **Submit the same day if possible** — don't wait for Aug 5 itself. Portals fail, files corrupt, wifi dies. Submitting a day early removes an entire category of risk.

### Day 5 (Aug 5) — Buffer / Submission Day
- Only needed if Day 4 submission wasn't possible. Final read-through, submit early in the day.

---

## Slide-by-Slide Content Draft

Map this to your SPOC's exact outline order — the *content* below is what matters; reorder freely to fit their template.

**1. Title Slide**
UrjaSetu · Problem Statement SVH26004 · Hybrid Renewable Energy Generation Solution · Team name, members, mentor.

**2. Problem Statement**
Restate in your own words, but echo the judges' own phrasing: campuses have solar + wind + battery running in isolation; no coordination layer; surplus is wasted, batteries run on fixed schedules, campuses still pull grid power at the worst times.

**3. Our Idea (the slide that must land in 10 seconds)**
"UrjaSetu is a vendor-neutral software layer that unifies a campus's solar, wind, battery, and grid connection into one coordinated Virtual Power Plant — forecasting supply and demand, and issuing plain-language recommendations to maximize self-consumption, with zero new hardware."

**4. Technical Approach / Architecture**
Insert the tech guy's architecture diagram here. Briefly narrate each block: adapter layer → data store → forecasting → optimization → recommendations → dashboard.

**5. What Makes This Different (USPs)**
- Vendor-neutral adapter layer (works with any inverter/turbine/battery brand)
- Explainable recommendations, not a black box
- What-if scenario simulator
- Built for statewide scale from day one (single-campus AND DTE aggregate view)
- Zero new hardware cost
- Human-in-the-loop — advisory, not autonomous control

**6. Feasibility & Viability**
- Software-only deployment on existing meters/inverters
- Regulatory tailwind: Rajasthan's RERC already allows net metering up to 500 kW, and its 2025 Third Amendment introduced Virtual Net Metering (VNM) and Group Net Metering (GNM) — meaning the "virtual power plant" concept maps onto an *actual current state policy mechanism*, not just a technical idea.
- Advisory-first design avoids safety/liability concerns for a government deployment.

**7. Impact & Benefits**
Frame numbers as illustrative estimates to be validated in a pilot: uncoordinated setups typically self-consume ~55–65% of renewable generation; coordinated dispatch can realistically push this to ~75–85%, with a direct ₹ and CO₂ payoff. Tie this to the "Clean & Green Technology" theme explicitly.

**8. Tech Stack**
React/FastAPI/TimescaleDB/Prophet-or-similar for forecasting/rule-based optimizer with a documented path to MILP or RL — keep this slide light, it's proof of feasibility, not the main event.

**9. Scalability Roadmap**
Single campus pilot → all DTE institutions → statewide rollout, with a real DISCOM/RERC integration path in the future.

**10. Team & References**
Team member roles, faculty mentor, and 2–3 source references (RERC net metering regulations, Rajasthan Clean Energy Policy 2024).

---

## Rapid Q&A Prep for the Pitch Person (Top 5 — Memorize These)

1. **"How is this different from just buying a bigger battery?"** → Bigger batteries without coordination logic still run on fixed schedules and miss real surplus/deficit windows — this is exactly the "orchestration, not procurement" distinction the problem statement itself draws.
2. **"How does this scale to 50 campuses, not just one?"** → Multi-tenant architecture, one adapter spec, a centralized DTE aggregate dashboard.
3. **"What if a campus has no internet?"** → Local edge fallback with cached rules; sync resumes when connectivity returns.
4. **"Why would a facility manager trust an AI recommendation?"** → Every recommendation shows its reasoning in plain language, and actions are advisory — a human confirms before anything happens.
5. **"What's the real deployment cost?"** → Software-only on existing meters/inverters; only new cost is a low-cost gateway device per site if a legacy device lacks a digital interface.

---

## Final Submission Checklist

- [ ] Deck matches SPOC's exact required format (file type, slide count, fonts if specified)
- [ ] Every team member's name/role is correctly listed
- [ ] All numbers are labeled as estimates where they are estimates
- [ ] File size under any stated portal limit
- [ ] Submitted at least a few hours before the actual deadline, not at the wire
- [ ] Pitch person has rehearsed out loud at least twice with a timer
