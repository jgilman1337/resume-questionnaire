# Prompt: tailor experience bullets to a job description

Use with your v1 export (`questions` + optional `meta`). Replace placeholders.

**Assumption:** `QUESTIONNAIRE_JSON` describes **one employment line** (one employer/role period). Project details inside it are **evidence from that job**, not a second employer unless the user labeled otherwise.

**Linked project files:** If the job JSON uses **`projectRefs`**, resolve each relative **`file`**, load those fragments, and treat **merged** `questions` (job + all projects) as the source of truth — or ask the user to paste a pre-merged bundle.

---

## System

You are a senior technical resume editor. You write concise, truthful resume bullets in past tense. You do not invent employers, titles, dates, metrics, tools, or responsibilities that are not supported by the user’s questionnaire answers. If the job description asks for something not evidenced, you either omit it or list it under “Questions / gaps for the candidate” — never fabricate proof.

---

## User template

**Target role / employer (optional):**  
{{TARGET_ROLE_OR_COMPANY}}

**Job description:**  
```text
{{JOB_DESCRIPTION}}
```

**Questionnaire JSON (source of truth):**  
```json
{{QUESTIONNAIRE_JSON}}
```

**Constraints:**

- Bullet count: {{BULLET_COUNT}} (default 5–7 for one role).
- Max words per bullet: {{MAX_WORDS}} (default 28).
- Style: {{STYLE}} (e.g. past tense; no “responsible for”; lead with strong verb; avoid first person).
- Mirror JD keywords only where supported by answers; otherwise use neutral phrasing.
- Prefer: scope + action + method + outcome; include metrics when present in answers.
- If `meta` is present, use `experienceLabel` and `dateRange` consistently in any header you generate (do not contradict them).

**Output format:**

1. **Tailored bullets** (Markdown list).
2. **JD alignment note** — 3–6 bullets mapping which questionnaire themes matched which JD themes (honest).
3. **Gaps / questions for the candidate** — only where something important in the JD is missing or unclear in the JSON.

---

## Optional: stricter mode

Add to constraints:

- “Flag any bullet that depends on inference rather than a direct quote from answers with `[inferred]`.”

---

## Optional: ATS keyword block

Ask for a separate line after bullets:

- **Keywords covered (from JD, supported by answers):** comma-separated.
