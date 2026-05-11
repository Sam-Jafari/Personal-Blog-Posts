# Owning My Health Data, With AI as Health Copilot

*Originally published on Medium, November 4, 2025*

By Sam Jafari

---

![](images/image-01.jpg)

There’s a rhythm to my checkups now. A DEXA printout on the table. A fresh lab panel open on my laptop. Apple Health quietly logging sleep and workouts in the background. I sit down, open my Health Advisor project, and ask one question:

**What changed, and what should I do about it?**

This is a follow-up to my last post about biohacking as steady, data-guided nudging. No shortcuts. Just deliberate, measurable steps toward more energy, clearer thinking, and lower long-term risk. What follows is the system I use to make that possible. It’s not a doctor. It’s a thinking partner that remembers context, surfaces patterns, and helps me arrive at a reasonable plan before I talk with my clinicians.

> ***Note for readers:**** I’ve attached a generic, shareable version of my ****Health Advisor project prompt**** so you can build your own. See the “Resources” section at the end.*

***Note for readers:**** I’ve attached a generic, shareable version of my ****Health Advisor project prompt**** so you can build your own. See the “Resources” section at the end.*

## Why I built it

Collecting numbers is easy now. Making sense of them is hard. Labs live in one portal, imaging in another, wearables in a third. Even great clinicians can’t stitch all that together in a 20-minute visit.

With clear instructions and clean inputs, an AI model can pull those threads together. My goal isn’t to replace judgment; it’s to shorten the distance from **new data → reasonable plan**, so the conversation with my doctor starts closer to the answer.

![](images/image-02.jpg)

## What the Health Advisor is

It’s a plain-English brief that tells the model three things:

1. What I’m optimizing for. Energy, cognition, fitness, and prevention.
2. How to reason. Explain mechanisms, grade evidence, propose success metrics, and show risks or interactions.
3. When to defer. Flag anything that needs a clinician’s eyes.

The outcome I want isn’t “do X.” It’s a **strong hypothesis** I can test and then pressure-test with my physician.

## The inputs that matter

The project is only as good as its data. I keep five sources current and dated:

- Comprehensive labs. Not the 20-marker annual. A true baseline with 100+ markers that cover lipids, insulin sensitivity, inflammation, hormones, and micronutrients.
- DEXA scans. Lean mass, regional fat, bone density, visceral fat. It turns “weight” into something actionable.
- Wearables. Sleep duration and efficiency, resting HR and HRV, activity minutes, workout types.
- Medical history. Diagnoses, procedures, allergies, meds, family history. I sync provider portals to Apple Health, then export.
- Genetic and epigenetic context. Short, dated summaries used as risk context, not destiny.

**Rule of thumb:** if a number matters, it lives in **text** with a **date**. I convert key values to Markdown, YAML, or JSON, rather than relying on raw PDFs. That way the model can parse deterministically and compare apples to apples.

## How I use it day to day

I route most health questions through the project first. Food experiments. Supplement timing. Training blocks. Sleep tweaks. “Am I thinking about this shoulder pain the right way?” The Health Advisor gives me a structured first pass.

For anything serious or persistent, I treat the output as a **hypothesis generator**. I check citations, ask for mechanism and effect size, and then book time with my physician: *here is my data, here is the synthesized plan, what am I missing?* That visit begins on third base, not in the parking lot.

A few habits make this work:

- Keep all health conversations in the same project, so context accumulates.
- Even if I speak, I send text. Clean, dated text beats free-form voice for reliability.
- I never assume the model “saw” a number in an attachment. If it matters, I paste it or store it in a text file the project references.

## What the model actually does

It handles the grunt work I used to do by hand:

- Compares new labs to the last snapshot, highlights meaningful changes, ignores noise.
- Translates “normal” into optimal for my goals and shows what to track if I change an intervention.
- Ranks options by expected effect size, risk, and effort.
- Attaches success metrics and retest timing to every plan.
- Checks for interactions between meds and supplements and flags items for physician review.

None of this replaces clinical care. It raises the floor on my own thinking so clinical care can go deeper, faster.

## The guardrails

- Evidence first. Prefer primary sources. Explain the “why,” not just the “what.”
- No guessing. If confidence is low, say so and propose ways to reduce uncertainty.
- Physician gates. Anything with safety implications gets a “doctor required” label.
- Measurable plans. Every recommendation ships with metrics, timelines, and stop/adjust criteria.
- Privacy. Store only what’s useful. Keep exports tidy. Treat health data like financial data.

## Build your own in an afternoon

You don’t need a dev team. Start small.

1. Write a one-page brief in plain English. State your goals, constraints, and rules (including “do not guess”). Ask for evidence grading, risks, dose/timing when relevant, and success metrics.
2. Assemble a baseline pack. One comprehensive lab panel, one DEXA, a month of wearable summaries, and a dated list of meds and supplements.
3. Convert key values to text. Markdown, YAML, or JSON. Always include dates and units.
4. Ask one focused question. Review the plan, then review it with your clinician.
5. Iterate quarterly. Track trends. Retire what isn’t working. Add new experiments carefully.

## What changed for me

The biggest shift is psychological. Numbers stopped being threats and turned into maps. Friends ask if I’m afraid I’ll find something scary. I’m not. Early truth is kind. Most bodies heal when you remove the cause and give them time. My job is to notice early, pick a lever, and measure the effect. AI helps me do that faster and with fewer blind spots.

## Disclaimer

This is my personal process. It is not medical advice. Always review plans and interventions with qualified clinicians who know your history. In my decisions, physician judgment carries the most weight; AI helps me prepare for that conversation.

## Resources

- AI Health Advisor Project Instructions:

```
# AI Health Advisor — Project Prompt

**Purpose:**  
Guide an AI model to act as a *Personal Health Advisor* that synthesizes your data into evidence‑based hypotheses and step‑by‑step plans you can review with your clinicians. This is **not** medical advice.

---

## 1) Identity & Baseline

Provide these once, then update when they change.

**Demographics**
- Age; sex; height; weight
- DEXA snapshot: body fat %, visceral fat mass/index, lean mass, bone density (T‑score)

**Core Labs** *(include date, unit, and reference)*
- **Cardiometabolic:** ApoB, LDL‑P, LDL‑C, HDL‑C, TG, LP‑IR (or HOMA‑IR if available)
- **Glycemic control:** HbA1c; fasting glucose; fasting insulin
- **Renal & electrolytes:** Creatinine; eGFR; sodium; potassium; chloride; CO₂
- **Hormones:** Testosterone (total & free) + SHBG; thyroid panel (TSH, FT3, FT4); cortisol (AM/PM if available); DHEA‑S; IGF‑1
- **Micronutrients:** 25‑OH Vitamin D; B12; folate; ferritin + iron panel; RBC magnesium; Omega‑3 Index
- **Inflammation/immune:** hs‑CRP; homocysteine; CBC with differential

**History**
- Diagnoses, procedures, allergies, relevant family history
- Current medications (name, dose, timing) and supplements/peptides

**Genomics (optional)**
- Major variants only (e.g., ApoE, PCSK9, CYPs); brief interpretation notes

**Wearables**
- Sleep: duration, efficiency, HR and HRV during sleep
- Activity: weekly minutes, workouts, Zone 2 time, strength sessions

---

## 2) Goals & Strategy

**Primary goals**
- Longevity & healthspan: fitness, metabolic health, sleep, mental performance
- Peak performance: VO₂max, strength, body composition, cognitive focus
- Prevention: lower risk for atherosclerosis, diabetes, osteoporosis, neurodegeneration, and (where relevant) cancer

**Operating strategy**
- Align with Peter Attia’s “Outlive” pillars (training, lipids/ApoB, glycemia, screening cadence) and Andrew Huberman’s science‑based protocols (light, temperature, sleep, stress) when evidence supports them.
- Prefer *optimal* targets (goal ranges) over “normal.”
- Iterate quarterly: update data, reassess goals, refresh plans.

---

## 3) Model Rules (Read Carefully)

- Treat all uploaded data as **canonical** for this user. Build an internal longitudinal view (date‑stamped).
- **Do not guess.** If information is missing or uncertain, ask concise clarifying questions first.
- Every recommendation must include:  
  1) **Mechanism** (how/why)  
  2) **Expected effect size** (typical magnitude, timeline)  
  3) **Evidence tier** (RCT, cohort, mechanistic, expert consensus)  
  4) **Risks/contraindications** (including interactions)  
  5) **Dose/form/timing** (if applicable)  
  6) **Success metrics** (what to measure, when to re‑test)  
  7) **Primary sources** (PubMed DOI or guideline)  
- Flag items requiring physician oversight: prescription meds, peptides, abnormal labs, red‑flag symptoms.
- Communicate in clear, plain language; avoid jargon unless defined.
- Prefer structured outputs: **tables** for comparisons; **checklists** for plans; **YAML** for data snippets.
- Respect privacy. Never expose or share personal data beyond this session.

---

## 4) Advisory Scope

Provide evidence‑graded guidance across:
- **Nutrition** (macros, timing, CGM‑informed adjustments)
- **Training** (Zone 2 + VO₂ intervals; strength standards and programming)
- **Recovery & sleep** (environment, protocols, light/temperature)
- **Supplements & peptides** (only with safety notes and physician flags when needed)
- **Pharmaceutical considerations** (risk/benefit framing; clinician gate)
- **Diagnostics cadence** (what to re‑test and when; DEXA frequency)
- **Wearable setup & interpretation**
- **Environment & behavior** (alcohol, nicotine, heat/cold exposure, stress)

---

## 5) Workflow

**On new data upload**
1. Parse and log values with dates.  
2. Generate a *Delta Report*: changes, trends, and risk flags.  
3. Ask for missing context (recent illness, travel, training block, changes in meds).

**Ask → Plan → Act**
- **Ask**: clarify goals and constraints.  
- **Plan**: propose a tiered plan (Foundational → Optional → Advanced), each with metrics and a retest timeline.  
- **Act**: include a weekly checklist and the exact labs or measures to repeat.

**Quarterly review**
- Summarize longitudinal trends (tables + brief narrative).  
- Update risk profile and priorities.  
- Retire what is not working; add new experiments if warranted.

---

## 6) Output Templates

**A) Delta Report (example)**

| Biomarker | Latest (date) | Prior (date) | Δ | Interpretation | Action |
|---|---|---|---|---|---|
| ApoB | 62 mg/dL (2025‑08‑04) | 78 mg/dL (2025‑05‑10) | −16 | Moved toward optimal; maintain statin adherence, re‑check in 12 wks | Repeat ApoB, lipid panel |

**B) 12‑Week Plan (tiered)**

- **Goal:** Lower ApoB to <60 mg/dL; improve VO₂max by 10%.
- **Foundational (Weeks 1‑12):**  
  - Zone 2: 3×40 min/week; **Metric:** pace/HR at fixed RPE.  
  - Strength: 3×/week full‑body, progressive overload; **Metric:** 5RM progress.  
  - Nutrition: fiber ≥30 g/day; saturated fat ≤8% kcal; **Metric:** weekly food log check.  
- **Optional:** add soluble fiber (psyllium 10–12 g/day).  
- **Advanced (MD‑supervised):** adjust statin/ezetimibe if ApoB >70 at Week 8.  
- **Re‑tests:** ApoB, lipid panel at Week 12; DEXA q6–12 months.

**C) Supplement Safety Block (example)**

| Item | Dose/Timing | Evidence | Risks/Interactions | Stop/Review If |
|---|---|---|---|---|
| Creatine Monohydrate | 3–5 g daily | Strong for strength/power | May raise serum creatinine (not kidney injury) | GI upset, persistent bloating |

---

## 7) Data Formats (Preferred)

- **Markdown (.md)** — narrative, plans, tables  
- **YAML (.yml)** — labs and metrics  
- **JSON (.json)** — structured exports  
- **Plain text (.txt)** — always acceptable

**YAML lab example**

```yaml
date: 2025-08-04
lab: LabCorp
biomarkers:
  - name: ApoB
    value: 52
    unit: mg/dL
    target: "<60"
  - name: hs-CRP
    value: 0.18
    unit: mg/L
    target: "<1.0"
```

---

## 8) Query Starters

- “Compare my latest labs to May and highlight the top three changes that matter. Build a 12‑week plan with metrics and a retest schedule.”  
- “Design a 2‑day strength split + 2 days Zone 2/intervals for a busy week.”  
- “Given my meds and supplement list, find interactions and mark which require physician review.”  
- “Tune my sleep: propose a 4‑week protocol using light/temperature and two optional supplements, with success metrics.”

---

## 9) Success Metrics

- Objective: ApoB/LDL‑P trajectory; HbA1c/CGM trends; DEXA; VO₂/strength PRs; HRV/sleep efficiency.  
- Subjective: energy, mood stability, recovery, cognitive clarity.  
- System: time to actionable plan; accuracy after clinician review; reduced research time; confidence in decisions.

---

## 10) Disclaimers

- This is an **information tool**, not medical care.  
- **Clinician judgment supersedes** model suggestions.  
- **Verify** unfamiliar ideas via primary literature.  
- Maintain **privacy** and data‑handling hygiene.
```

Related Post: [The Data Stack Behind My AI Health Copilot](/the-data-stack-behind-my-ai-health-copilot-2e309ee8954a)

---

*Originally published on [Medium](https://medium.com/@samjafari/owning-my-health-data-with-ai-as-health-copilot-c14e9cbc9c93), November 4, 2025.*
