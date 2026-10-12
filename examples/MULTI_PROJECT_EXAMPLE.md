# Many projects, **one** employer

You have **one** resume line: `Acme — Engineer — 2020–Present`. All project evidence belongs to **that** employment — not separate “jobs.”

---

## Preferred: linked files + `projectRefs`

Put job-level answers in **`acme-engineer-2020-present.json`**, list projects in **`projectRefs`**, and store each project in **`projects/<slug>.json`**.

- **No** `[Project: …]` prefixes required inside question strings.
- Full convention: **`LINKED_PROJECTS.md`**
- Working example: **`linked-projects/`** (Riverbank sample)

---

## Alternative: one JSON file (flat list)

Keep a **single** file and repeat the three project prompts (or full section H) for each project. Disambiguate with **`[Project: Name]`** in the `question` string (or prefix answers only).

Use this if you want zero path resolution and one file to copy-paste into a chat.

---

## What you do **not** do

- Orphan project files **without** a parent job JSON that references them via **`projectRefs`** (unless it is a **side** project — different rules; see **`README_PER_ROLE.md`**).

---

## Tailoring to a job posting

Resolve **`projectRefs`**, merge job + project `questions` for the LLM (or multi-attach). Same employer data; JD changes per application.
