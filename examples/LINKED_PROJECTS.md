# Linked project files (preferred for many projects)

If you do not want repeated `[Project: …]` prefixes in one giant `questions` array, split **each project** into its own JSON file and **link** it from the job file.

---

## Layout

```text
your-data/
  acme-engineer-2020-present.json    ← job: meta, job-level questions, projectRefs
  projects/
    refunds.json
    ledger-api.json
    ci.json
```

---

## Job file (`…job.json`)

- **`questions`:** only prompts that apply to the **whole** employment (title, employer, overall outcomes, tools, themes, etc.).
- **`projectRefs`:** optional array. Each entry:
  - **`file`** (required): path **relative to the job JSON file** (e.g. `projects/refunds.json`).
  - **`id`** (optional but recommended): stable slug; should match **`projectMeta.id`** in the linked file.

Validate with **`schemas/resume-questionnaire-export.schema.json`**.

---

## Project file (`…/projects/refunds.json`)

- Same **`schemaVersion`** as the job export.
- Optional **`projectMeta`:** `id`, `name`, `parentJobFile` (relative path back to the job file — for humans/tools).
- **`questions`:** section **H** prompts (or the three from `fillable-15`) **without** embedding the project name in every question string — the filename / `projectMeta` disambiguates.

Validate with **`schemas/resume-project-fragment.schema.json`**.

---

## Sending data to an LLM

JSON has no built-in `#include`. Before filling `{{QUESTIONNAIRE_JSON}}` in **`prompts/tailor-bullets.md`**, either:

1. **Merge** for one prompt: concatenate job `questions` + each linked file’s `questions` (and optionally add a heading comment in a wrapper object), or  
2. **Multi-part prompt:** pass the job JSON and each project file as separate attachments with instructions to treat them as one employment.

Your app should resolve **`projectRefs`** by reading each **`file`** path relative to the job file.

---

## Example in this package

See **`linked-projects/`**:

- `riverbank-senior-engineer-2021-present.json`
- `projects/refund-hardening.json`, `ledger-read-api.json`, `ci-migration.json`

---

## Flat alternative (single file)

You can still put every project in **`questions`** with `[Project: …]` prefixes — see **`README_PER_ROLE.md`**. Linked files are optional; use whichever fits your editor and tooling.
