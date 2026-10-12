# Resume questionnaire package

A single source of truth for a **fill once, tailor many times** resume workflow: answers export to JSON for AI-assisted bullets tailored to job descriptions.

**Step-by-step “what do I do for each job on my resume?” → read [`README_PER_ROLE.md`](README_PER_ROLE.md) first.**

## What one export is for (read this first)

| This package is **for** | This package is **not** (by default) |
|-------------------------|--------------------------------------|
| **One job** = one line on your resume: one employer, one title block, one set of dates (one employment stint). | A standalone “project-only” dossier, unless you deliberately use it that way (e.g. side work). |
| **Projects** = **evidence inside that job**: section **H** (and the three project prompts in `fillable-15.json`) describe **work you did while employed there**—repeat the block per major project. | A replacement for “one JSON for your whole career.” |

**Practical rule:** duplicate the questionnaire **once per job** on your resume. For each job, add **one or more project blocks** (same questions, different answers—prefix the `question` text with the project name if needed). **Section R** and similar are for **side projects / portfolio** when that is not a paid job. **Targeting the market** (section **A**) can live in a separate global file or the first job export—your choice.

## Quick start

1. Read **`README_PER_ROLE.md`** — one checklist per employment line (file naming, projects, applications).
2. Read **`GUIDE.md`** — tiered checklist (you do **not** need all 202 prompts).
3. Fill prompts from **`QUESTIONNAIRE.md`** (sections **A–AB**).
4. Export v1 JSON and validate against **`schemas/resume-questionnaire-export.schema.json`**.
5. Use **`prompts/tailor-bullets.md`** with your JSON + a job description.

## Contents

| Path | Purpose |
|------|---------|
| **`README_PER_ROLE.md`** | **What to do per job on your resume** (one JSON per employer; how projects and applications fit). |
| `GUIDE.md` | Tier 1 / 2 / 3 — what to fill first; repeatable blocks. |
| `QUESTIONNAIRE.md` | Full question bank (**202** numbered prompts). |
| `schemas/resume-questionnaire-export.schema.json` | JSON Schema for v1 export (optional **`projectRefs`**). |
| `schemas/resume-project-fragment.schema.json` | JSON Schema for **one project file** linked from a job export. |
| `schemas/resume-questionnaire-v2.schema.json` | Optional structured model (sections, IDs). |
| `examples/export.minimal.json` | Smallest valid v1 example. |
| `examples/export.full.json` | Richer example with `meta` + many Q/A pairs. |
| `examples/fillable-15.json` | **15 prompts** — one **job** + one **project** (empty answers); see `meta.notes`. |
| `examples/WORKFLOW_EXAMPLE.md` | **Walkthrough:** two jobs → two JSON files → one application (no new fact file). |
| `examples/LINKED_PROJECTS.md` | **Linked project files** — `projectRefs` + relative paths (preferred for many projects). |
| `examples/linked-projects/` | Example job JSON + `projects/*.json` fragments. |
| `examples/MULTI_PROJECT_EXAMPLE.md` | Short comparison: linked vs flat single-file pattern. |
| `prompts/tailor-bullets.md` | Prompt template for JD-tailored bullets. |

## Export format (v1)

```json
{
  "schemaVersion": "1.0.0",
  "questions": [
    { "question": "…", "answer": "…" }
  ]
}
```

Optional: include **`meta`** (`experienceLabel`, `dateRange`, `location`, `notes`) alongside `schemaVersion` and `questions`. When `meta` is present, `schemaVersion` is required. See `examples/export.full.json`.

## Validation

Use any **JSON Schema Draft 2020-12** validator against `schemas/resume-questionnaire-export.schema.json` (e.g. `ajv` in CI, or editor integration).

## Versioning

- **Export v1:** `schemaVersion` **1.0.0** — flat `questions` array; optional `meta`; optional **`projectRefs`** (paths to project fragment JSON files — see `examples/LINKED_PROJECTS.md`).
- **Project fragments v1:** `resume-project-fragment.schema.json` — `questions` + optional `projectMeta` for linked files.
- **V2 schema** (`resume-questionnaire-v2.schema.json`): **2.0.0** — sections/items for apps that need stable IDs.
