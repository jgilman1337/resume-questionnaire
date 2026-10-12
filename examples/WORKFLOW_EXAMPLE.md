# Example: two jobs on your resume + one application

Fictional person **Alex**. They want **two** employment lines on the CV: current job and previous job. They apply to **one** company posting.

---

## File layout (facts you maintain)

```text
resume_questionaire/
  alex-data/
    riverbank-senior-engineer-2021-present.json   ← current job (facts)
    northwind-mid-engineer-2018-2021.json       ← previous job (facts)
```

Each file is **one employer**. Names are arbitrary; the important part is **one JSON per resume line**.

---

## `riverbank-senior-engineer-2021-present.json` (excerpt)

One **`meta`** block identifies the job. **`questions`** hold answers **only** for Riverbank.

```json
{
  "schemaVersion": "1.0.0",
  "meta": {
    "experienceLabel": "Riverbank Payments — Senior Software Engineer",
    "dateRange": "Mar 2021 – Present",
    "location": "Remote (US)"
  },
  "questions": [
    {
      "question": "Employer name (and parent company if known/acquired).",
      "answer": "Riverbank Payments"
    },
    {
      "question": "Why did this project exist (problem statement)?",
      "answer": "Refund pipeline had duplicate credits under load; needed reliability + observability."
    },
    {
      "question": "What was uniquely yours on this project?",
      "answer": "Owned the retry/idempotency design and the cutover plan with Risk."
    }
  ]
}
```

*(In real use you’d have the full `fillable-15` or full bank filled out.)*

---

## `northwind-mid-engineer-2018-2021.json` (excerpt)

**Different file**, **different employer** — no mixing.

```json
{
  "schemaVersion": "1.0.0",
  "meta": {
    "experienceLabel": "Northwind LLC — Software Engineer",
    "dateRange": "Jun 2018 – Feb 2021",
    "location": "Chicago, IL"
  },
  "questions": [
    {
      "question": "Employer name (and parent company if known/acquired).",
      "answer": "Northwind LLC"
    },
    {
      "question": "List up to 10 measurable outcomes tied to your work (metric + before/after or absolute result).",
      "answer": "Reduced batch job runtime from 6h to 45m; cut failed nightly runs by ~60%."
    }
  ]
}
```

---

## Applying to **one** job posting (no new fact file)

Alex finds a posting at **Contoso** and copies the job description text.

**They do not** create `contoso-application.json` for facts.

They run the tailor prompt (see **`prompts/tailor-bullets.md`**) with:

1. **`JOB_DESCRIPTION`** = Contoso’s posting (text).
2. **`QUESTIONNAIRE_JSON`** = often **one file at a time** per experience section, e.g. first run with `riverbank-…json` to generate Riverbank bullets, then with `northwind-…json` for Northwind bullets — **or** a single merged JSON if their tool expects that.

Same two employer files, **many** applications: only the **JD text** and the **prompt** change.

---

## One-liner summary

| Situation | What you create |
|-----------|-------------------|
| New paid job to list on CV | **New** `employer-title-dates.json` |
| Second project at same employer | **More answers** in the **same** file (duplicate project rows or prefix) |
| New job application / new posting | **No** new facts file — reuse JSON + paste new JD |

See also: **`README_PER_ROLE.md`**, **`export.full.json`** (single-job rich example), **`LINKED_PROJECTS.md`** / **`linked-projects/`** (many projects via separate files + `projectRefs`).
