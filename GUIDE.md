# How to use this package (without drowning)

## Scope: one JSON file = one job (projects go inside)

For a **numbered checklist** (naming files, repeating for each employer, and what happens when you apply somewhere), use **`README_PER_ROLE.md`**.

- **Unit of work:** one filled export describes **one employment line** (employer + role + dates): the context for **that** stint.
- **Projects:** prompts in section **H** (and the three project lines in `fillable-15.json`) are **not** a separate top-level resume line—they are **examples and proof** **under** that job. Use **one** flagship project in the short form, or **repeat** section H for 2–3 projects (prefix each `question` with the project name).
- **Exceptions:** **side projects / community** → section **R** (or a dedicated export you label as non-employment). **“What job I want next”** (section **A**) is about **your search**, not one employer—keep it in one global doc or repeat only where useful.

`QUESTIONNAIRE.md` is a **bank** of **202** numbered prompts (sections **A–AB**), not a mandatory form. Export only `{ question, answer }` pairs you actually fill.

## Tiers (suggested)

### Tier 1 — “Good enough to generate first bullets” (~35–50 answers)

Prioritize:

- **A:** targets, themes, what to de-emphasize (a subset).
- **B:** title, employer, dates, location, employment type.
- **C:** what the company does, what you affected, rough scale.
- **D:** team size, stakeholders, on-call if relevant.
- **E:** hired to do vs actually did; standing responsibilities; tools you lived in.
- **F:** what you owned end-to-end vs contributed; decisions you owned.
- **G:** measurable outcomes, proxies if metrics are confidential, headline metric.
- **H:** at least **one** project block (questions through launch/tech/aftermath).
- **P:** tools/methods/domains you can defend; optional paste of a sample JD.

### Tier 2 — “Strong tailoring + interviews”

Add:

- Second and third **H** project blocks (prefix questions with project name in the `question` string).
- **I** (practices: testing, CI/CD, incidents).
- **L** (collaboration, communication, conflict/alignment).
- **M** (mistakes, learning — professional framing).
- **N** (promotion, artifacts, talks).
- **O** (skeptic prep, fair credit split).
- **Z** (2–3 STAR stories as data).

### Tier 3 — “Specialist / senior / staff depth”

Fill as needed:

- **J, K** (data/ML, customer/sales/legal).
- **T–V** (deep tech, migrations, cost/performance).
- **W** (security/compliance).
- **X** (product/UX overlap).
- **Y** (management/leadership).
- **AA** (keyword honesty grid).
- **Q, R, S, AB** (education, side projects, logistics, private notes).

## Repeatable blocks

- **Projects:** (1) **Linked:** `projectRefs` in the job file → one JSON per project under e.g. `projects/` — see **`examples/LINKED_PROJECTS.md`** and **`examples/linked-projects/`**. (2) **Flat:** duplicate section **H** in one file; prefix `question` with `[Project: Aurora] …` — see **`examples/MULTI_PROJECT_EXAMPLE.md`**.
- **Per-tech deep dives:** duplicate section **T** for PostgreSQL, Kubernetes, etc.

## JSON tips

- Omit pairs with empty `answers` to save tokens.
- Use `meta` in export when you want consistent headers (`experienceLabel`, `dateRange`, `location`) — see `schemas/resume-questionnaire-export.schema.json`.
- For structured UIs, consider migrating to v2 (`schemas/resume-questionnaire-v2.schema.json`).

## Fifteen-question fast path

`examples/fillable-15.json` is a **fillable subset** of the bank (empty `answer` fields). It covers: positioning themes, role header, company context, hired vs actual, ownership, quantified outcomes + headline metric, one flagship project (problem → your slice → result), skeptic prep, and interview-defensible tools. Prefix project-related answers with the project name if you track multiple projects.

## File map

| File | Role |
|------|------|
| **`README_PER_ROLE.md`** | **What to do per resume job** (workflow) |
| `QUESTIONNAIRE.md` | Master prompt list |
| `examples/export.minimal.json` | Minimal valid v1 |
| `examples/export.full.json` | Rich fictional example |
| `examples/fillable-15.json` | 15-prompt starter template |
| `prompts/tailor-bullets.md` | LLM prompt for JD tailoring |
| `schemas/*.json` | Validation |
