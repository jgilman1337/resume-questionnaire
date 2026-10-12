# Per-job workflow — what to do for **each** line on your resume

**This is the separate workflow readme** for this folder. It answers: *“What exactly do I do per role?”* — meaning **one employment line** (one employer + dates), not every job posting you apply to.

Package index: **`README.md`**. Depth/tiers: **`GUIDE.md`**. **Concrete walkthrough (two employers, one application):** **`examples/WORKFLOW_EXAMPLE.md`**. **Many projects (linked files):** **`examples/LINKED_PROJECTS.md`**.

---

**“A role” here means one employment line** — one employer, one contiguous (or phased) stint, one block of dates on your CV. It does **not** mean “every job posting you apply to.”

---

## The rule in one sentence

**For each paid job you want on your resume, you create and maintain exactly one questionnaire export (one JSON)** for that job. Projects you did at work live **inside** that JSON, not as separate top-level “jobs.”

---

## Per job: do this checklist

### 1. Create a dedicated file for this employment

- Copy **`examples/fillable-15.json`** for a fast pass, **or** work from **`QUESTIONNAIRE.md`** for the full bank.
- Save it with an unambiguous name, for example:  
  `acme-senior-engineer-2021-present.json`  
  (pattern: `employer-short-title-dates.json`).

### 2. Fill `meta` (so you never mix employers)

Set at minimum:

- **`experienceLabel`** — e.g. `Acme Corp — Senior Software Engineer`
- **`dateRange`** — e.g. `Mar 2021 – Present`
- **`location`** — if you want it on the resume

This reminds you (and any tool) **which job** this file describes.

### 3. Answer questions for **this job only**

- Everything in this file is about **that employer and that period**.
- **Do not** paste answers from a different company into this file.

### 4. Add **projects** that happened **at this job**

**Still one employment line** — but you can store projects in **separate files** and **link** them from the job JSON (recommended if you have many projects).

#### Option 1 — Linked files (**preferred** when you dislike long flat lists)

1. Keep **job-level** answers in the main file: `meta`, `questions` (title, employer, dates, overall metrics, tools, etc.).
2. Add a **`projectRefs`** array on the job file. Each item has **`file`** (path **relative to the job JSON**, e.g. `projects/refunds.json`) and optionally **`id`**.
3. Put each project’s `{ question, answer }` pairs in its **own** file under e.g. `projects/`. Questions can stay **plain** (no `[Project: …]` prefix) because the file name / `projectMeta` identifies the project.
4. Validate with **`schemas/resume-questionnaire-export.schema.json`** (job) and **`schemas/resume-project-fragment.schema.json`** (each project).

**Docs + example:** `examples/LINKED_PROJECTS.md` and `examples/linked-projects/`.

Before sending to an LLM, **merge** job + linked files into one payload, or attach **multiple** JSON parts — see `prompts/tailor-bullets.md`.

#### Option 2 — One file, flat list (no linking)

Duplicate the same three (or full section **H**) prompts **per project** in one `questions` array; disambiguate with **`[Project: Name]`** in the `question` string or in the answer. See **`MULTI_PROJECT_EXAMPLE.md`**.

**Do not** use **one separate file per project** **without** a parent job file that lists **`projectRefs`** — the job file is still the anchor for that resume line.

**Non-work** side projects: use **section R** or a **separately labeled** file; see below.

**Resume vs questionnaire:** Your CV might show **3–5 bullets** for one job while your data holds **6+ projects** — that is fine. The JSON is the **evidence locker**; tailoring picks which stories matter for each posting.

### 5. Export / save the JSON

- Remove empty `answer` strings if you want a smaller file (optional).
- Keep **`schemaVersion`** `1.0.0` unless you change your tooling.

You now have **one source-of-truth file per resume line**.

### 6. Repeat steps 1–5 for **each** job on your resume

| Resume line | Your action |
|-------------|-------------|
| Job 1 (e.g. current) | One JSON file |
| Job 2 (previous) | A **second** JSON file |
| Job 3 | A **third** JSON file |
| … | … |

**Never** merge unrelated employers into one export unless you are intentionally building a weird bundle (not recommended).

---

## What you do **not** do per job

- **You do not** create a new JSON **for every job posting** you apply to. The same employer file is reused.
- **You do not** put “the job I want next” (career goals) inside every employer file unless you want duplication. Prefer **one** global note or use **section A** once — see `QUESTIONNAIRE.md`.

---

## When you **apply** to a specific posting (different meaning of “role”)

This is **not** a new questionnaire. You already have the facts.

1. Pick the **relevant** employment JSON(s) for the resume you are building (often the last 1–3 jobs).
2. Paste the **job description** for the **opening** you want.
3. Run your AI prompt using **`prompts/tailor-bullets.md`**: pass **that employer’s JSON** (or a merged bundle your tool supports) + **that posting’s JD**.

So: **one questionnaire file per job on your CV**; **many tailoring passes** per file using different job descriptions.

---

## Side projects, freelancing, and non-employment work

- Use **section R** in `QUESTIONNAIRE.md`, **or**
- A **separate** JSON file you clearly label (e.g. `side-project-video-app.json`) so it is not confused with a W-2 job.

---

## Quick reference

| Question | Answer |
|----------|--------|
| How many JSON files per employer? | **One** (maintained over time). |
| How many projects? | **Unlimited** — either **linked files** (`projectRefs` + `examples/linked-projects/`) or **one file** with `[Project: Name]` prefixes (`MULTI_PROJECT_EXAMPLE.md`). |
| How many JSON files per job **application**? | **Zero new fact files** — reuse the same employer JSON + new JD in the prompt. |
