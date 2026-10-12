# Resume questionnaire (question bank)

## What this document is for

- **Primary use:** capture material for **one resume line** — **one paid job** (one employer + one role block + dates). Project questions (**section H** and related) describe **work you did during that job**, not a separate employer.
- **Multiple jobs on your resume:** use **one questionnaire copy (or one JSON export) per job**.
- **Multiple projects at the same job:** repeat **section H** for each major project; disambiguate by prefixing the `question` text with the project name (see “Using this file with JSON export” at the end).
- **Side projects, volunteering, portfolio:** use **section R** (and optionally **Q**) — or a separate export you label as non-employment.

Use **one copy per employer/role** (or duplicate and adjust). Skip any question that does not apply; empty answers can be omitted on export.

Each line below is intended as a **single `question` string** in JSON (you may shorten wording in your app if you keep meaning).

---

## A. Career targets & positioning

1. What job titles or levels are you targeting next (be specific: e.g. Staff Engineer, EM L5)?
2. Which industries or company stages are you prioritizing (startup, growth, enterprise, public sector)?
3. What geographic or remote constraints do you have?
4. In one sentence, what problem do you most want your next role to solve for an employer?
5. What three themes should a reader take away from your resume in the first 10 seconds?
6. What narrative arc connects your last 2–3 roles (promotion, pivot, deepening specialty)?
7. What do you want to be **known for** professionally (2–4 phrases)?
8. What should recruiters or hiring managers **stop** assuming about you that is wrong?
9. What topics do you want to **de-emphasize** even if they were a large part of past jobs?
10. Are you open to management, IC, or hybrid tracks—and what is your default preference?
11. What compensation or scope floor matters to you (only what you are comfortable writing down)?
12. What would make you say “no” to an otherwise good offer (culture, stack, travel, ethics)?

---

## B. Role header & logistics

13. Exact job title(s) as you want them on the resume (include level if relevant).
14. Employer name (and parent company if known/acquired).
15. Employment type (full-time, contract, consulting, internship).
16. City/state/country or “Remote” as you want it shown.
17. Start date (month/year) and end date or “Present”.
18. Did the title or scope change during this employment? Describe each phase with dates.
19. Why did you take this role (what were you optimizing for at the time)?
20. Why did you leave, or why are you considering leaving (neutral, factual phrasing)?
21. Would you rehire your past self for this role—why or why not?

---

## C. Company, product, and business context

22. In plain language, what does the company do and who pays for it (B2B, B2C, internal)?
23. What is the product or service your work most affected (name it like a user would)?
24. What was the approximate scale that mattered for your work (users, revenue band, requests/day, data volume—rough is fine)?
25. Who were the primary users or customers of what you built (personas)?
26. What regulatory, security, or compliance context applied (HIPAA, PCI, SOC2, GDPR, etc.)—if any?
27. What was the competitive or strategic pressure (speed to market, cost, reliability, differentiation)?
28. What was broken or missing before you joined that your team was trying to fix?
29. How did success get measured at the company level (OKRs, KPIs you were aware of)?
30. What major company events occurred during your tenure (funding rounds, layoffs, pivots, acquisitions)—only if relevant to your story?

---

## D. Org, team, and reporting

31. What was your team called, and where did it sit in the org chart (product line, platform, infra)?
32. How large was your immediate team (ICs, leads, managers)?
33. How large was the broader engineering org (order of magnitude)?
34. Who did you report to (role, not name) and who reported to you—if anyone?
35. Which cross-functional partners did you work with regularly (PM, design, data, support, sales, legal)?
36. How were decisions made (top-down, consensus, RFCs, guilds, incident-driven)?
37. What meetings or rituals anchored your work (sprint planning, roadmap reviews, design reviews, incident reviews)?
38. Were you on-call? Describe rotation length, severity of pages, and ownership boundaries.
39. Did you participate in hiring? In what capacity (phone screens, loops, debriefs, sourcing)?
40. Did you mentor, onboard, or lead interns? Describe scale and outcomes.

---

## E. Role definition: what you actually did

41. In 2–3 sentences, what were you hired to do?
42. In 2–3 sentences, what did you **actually** end up doing (often broader/narrower)?
43. What was explicitly **in scope** for your role?
44. What was explicitly **out of scope** but you still influenced?
45. What percentage of time (rough) went to: new features, maintenance, incidents, meetings, mentoring, tech debt?
46. What were your standing responsibilities week to week?
47. What were your biggest one-off initiatives or projects?
48. What did “done” look like in your context (shipping, adoption, SLO, customer outcome)?
49. What tools or systems did you live in daily (IDE, ticketing, CI, observability, CRM, data warehouse)?
50. What would your manager say you were uniquely responsible for?

---

## F. Ownership, autonomy, and decision rights

51. What did you own end-to-end (codebase, service, product area, process)?
52. What did you contribute to without owning?
53. What decisions could you make without approval?
54. What decisions required director/VP/architecture review?
55. Describe a decision you owned that had meaningful downside risk if wrong.
56. Describe a time you disagreed with a stakeholder and how it resolved.
57. How much ambiguity did you operate under (requirements, metrics, priorities)—low/medium/high with examples?
58. Did you set technical direction for others (patterns, standards, RFC outcomes)? Give examples.
59. Did you influence roadmap or prioritization? How (data, customer evidence, cost of delay)?
60. Did you manage budget or vendor selection (cloud spend, SaaS tools)? Describe.

---

## G. Impact: outcomes, metrics, and proof

61. List up to 10 measurable outcomes tied to your work (metric + before/after or absolute result).
62. For outcomes where numbers are confidential, what **ranges or directional** statements are still truthful?
63. What qualitative outcomes can you support (customer quotes, internal awards, leadership recognition)?
64. What was the **business impact** of your top 3 wins (revenue, cost, risk reduction, time-to-market)?
65. What was the **user impact** of your top 3 wins (latency, reliability, UX, accessibility)?
66. What **team impact** did you have (velocity, fewer incidents, simpler operations, better onboarding)?
67. What did you improve in reliability or uptime (SLOs, MTTR, error budgets)—with numbers if possible?
68. What did you improve in performance (latency p95/p99, throughput, cost per request)?
69. What did you improve in developer experience (build time, deploy frequency, flaky tests reduced)?
70. What adoption metrics moved because of your work (DAU, activation, retention, expansion)—if applicable?
71. What did you automate or eliminate (toil hours/week, manual steps, headcount avoided)?
72. If you had to pick **one** headline metric for this role, what would it be?

---

## H. Projects (repeat this block for each major project: Project 1, 2, 3…)

### H1. Project identity

73. Project name (internal or customer-facing).
74. One-line summary suitable for a resume sub-bullet context.
75. Timeline (start–end) and whether it shipped, was canceled, or evolved.
76. Why did this project exist (problem statement)?
77. Who asked for it (customer, exec, PM, engineering initiative)?
78. What would have happened if nobody did this project?

### H2. Your role on the project

79. Were you driver, contributor, advisor, or maintainer after launch?
80. Who else was on the core team (roles, not names)?
81. What was uniquely yours on this project?
82. What work did you do that others might not know about (glue work, docs, coordination)?
83. Did you hand off the project? To whom and in what state?

### H3. Execution details

84. What were the hardest technical challenges?
85. What tradeoffs did you make (speed vs quality, build vs buy, scope cuts)?
86. What risks did you mitigate (security, data loss, downtime, compliance)?
87. What unknowns did you have to research or prototype?
88. What did you cut from scope and why?
89. How did you validate the solution (experiments, dogfood, beta, A/B, shadow traffic)?

### H4. Technologies (per project)

90. List every technology materially used (languages, frameworks, infra, data stores, messaging).
91. For each major technology: what did it let you accomplish that would have been harder otherwise?
92. For each major technology: what was painful or limiting?
93. Would you choose the same stack again for a similar problem—why or why not?
94. Any notable libraries, internal platforms, or codegen tools that mattered?

### H5. Launch and aftermath

95. How was it deployed or released (feature flags, gradual rollout, migration windows)?
96. What broke in production, if anything, and how did you respond?
97. What metrics moved post-launch (or what qualitative signal confirmed success)?
98. What follow-up work did you or others do after v1?
99. What would you redo if you had a time machine (process or technical)?

---

## I. Engineering practices & quality

100. How did you approach testing (unit, integration, e2e, load)—what was the standard you pushed for?
101. How did you approach code review—what did you typically catch or teach?
102. How did you approach observability (logs, metrics, traces, alerts)—what did you instrument?
103. How did you approach incidents (postmortems, action items, prevention)?
104. Did you reduce tech debt in a deliberate way? Describe one refactor/migration with impact.
105. Did you improve CI/CD (pipeline speed, deployment frequency, rollback safety)? Quantify if possible.
106. Did you introduce or improve coding standards, linters, architecture guidelines?
107. Security: what threats did you consider (authn/z, secrets, SSRF, injection, supply chain)?
108. Privacy: did you handle PII/PHI—what safeguards did you implement or respect?
109. Accessibility or internationalization: did you ship improvements—what and why?

---

## J. Data, ML, and analytics (if applicable; skip otherwise)

110. What data sources did you work with (warehouses, lakes, streams, OLTP)?
111. What pipelines or ETL did you own or touch?
112. What dashboards or analyses informed decisions (tools: Tableau, Looker, Metabase, etc.)?
113. Did you run experiments (A/B, multivariate)? How did you interpret results responsibly?
114. Did you build or consume ML models—what was your role (training, serving, evaluation)?
115. What data quality issues did you encounter and how did you address them?

---

## K. Customer-facing & business partnership

116. Did you talk directly to customers or users? In what format (calls, onsite, support escalations)?
117. Did you participate in sales or solutions engineering? Describe responsibilities.
118. Did you translate customer pain into engineering work? Give an example.
119. Did you work with finance, legal, or procurement (contracts, DPAs, vendor reviews)?
120. Did you participate in pricing, packaging, or roadmap tradeoffs?

---

## L. Collaboration, leadership, and communication

121. How did you communicate progress (status updates, demos, written updates)?
122. Describe a time you aligned multiple teams toward a shared deadline.
123. Describe a time you mediated conflict or mismatched expectations.
124. How did you give feedback to peers or leadership—what was the outcome?
125. Did you present to executives or external audiences? On what topics?
126. Did you write docs, RFCs, playbooks, or training that others adopted?
127. Did you facilitate meetings or drive rituals (incident command, sprint ceremonies)?
128. What languages did you work in (human languages) if relevant to the role or market?

---

## M. Challenges, mistakes, and learning

129. What was the hardest part of this job for you personally?
130. What mistake did you make—what happened, what you learned, what changed after?
131. What project failed or under-delivered—what would you tell a hiring manager truthfully?
132. What skill gap did you close while in the role?
133. What feedback did you receive in performance reviews (themes, not confidential scores)?
134. What would you do differently with hindsight (process, communication, technical approach)?

---

## N. Recognition, scope growth, and artifacts

135. Promotions, title changes, or scope increases—dates and triggers.
136. Awards, spot bonuses, public recognition—what for?
137. Patents, publications, talks, podcasts—titles and venues (links optional).
138. Open source: repos, contributions, maintainer roles (scope of contribution).
139. Blog posts or internal tech talks—topics and approximate dates.
140. Notable artifacts: design docs, standards, libraries, templates you authored that others used.

---

## O. Differentiation, honesty, and “skeptic” prep

141. What might a skeptical interviewer doubt—what evidence addresses that doubt?
142. What parts of your impact were **team** vs **individual**—split credit fairly.
143. What buzzwords appear on your resume that you can defend with stories (define each in one line)?
144. What are you **not** trying to claim (boundaries)?
145. If you could change one thing about this role or company while you were there, what would it be—and what does that say about what you value?
146. What kind of work energizes you vs drains you (still at a professional level)?

---

## P. Job-description tailoring hooks (keywords & mapping)

147. List tools, frameworks, and cloud services you can defend in interview (comma-separated or bullets).
148. List methodologies you practiced truthfully (Agile, Scrum, Kanban, Shape Up, Shape-like, Lean, DevOps, SRE practices).
149. List domains you have depth in (payments, ads, streaming, healthcare, fintech, developer tools, etc.).
150. List “responsibility verbs” that match you (owned, led, mentored, architected, operationalized, migrated, optimized).
151. Paste a sample target job description (or bullet list) you care about—what matches strongly vs weakly?
152. What gaps will you need to address honestly in applications (tool never used, domain never shipped)?

---

## Q. Education, certifications, and earlier context (optional)

153. Highest relevant education—institution, degree, field, graduation year.
154. Coursework, thesis, or projects worth mentioning for specific applications.
155. Certifications (AWS, CKA, PMP, etc.)—year earned and whether still relevant.
156. Earlier roles: one line each if you need continuity for narrative (company, title, what you learned).

---

## R. Side projects & community (optional)

157. Side projects: problem, stack, users, outcome (even if small).
158. Meetups, community organizing, volunteering related to tech—role and impact.
159. Non-traditional background elements worth framing positively (career change, bootcamp, self-taught)—your narrative.

---

## S. Logistics for applications

160. Work authorization / sponsorship needs—only if you want this captured for private prompts.
161. Travel or relocation willingness—if relevant.
162. Links you use everywhere (LinkedIn, GitHub, portfolio)—for consistent generation.
163. Preferred bullet style (sentence case; past tense; avoid “responsible for”; max words per bullet).

---

## T. Deep dive: one technology or system (repeat per major tech: e.g. PostgreSQL, Kubernetes, Kafka)

164. Name of the technology/system and your proficiency level (learned on job vs expert).
165. What did you build, configure, or operate with it—be specific (not “used X”)?
166. What production incidents or surprises involved this technology—how did you troubleshoot?
167. What configuration or tuning decisions did you make (with rationale)?
168. What alternatives did you consider—why did you pick this one?
169. What would you audit first if you inherited this system tomorrow?

---

## U. Migrations, rewrites, and cutovers

170. Describe your largest migration (data, service, framework, cloud region)—scope and risk.
171. What was the rollback plan—and did you ever roll back?
172. How did you validate correctness (reconciliation, dual writes, shadow reads)?
173. What downtime or customer-visible effects occurred—how did you minimize them?
174. Timeline: planned vs actual; what caused variance?

---

## V. Cost, performance, and capacity

175. Did you reduce cloud or infra costs—how much (percent or dollars if shareable)?
176. Did you do capacity planning or load testing—what did you learn?
177. Did you fix a bottleneck—what was it before/after (profiling evidence)?
178. Did you implement caching, batching, deduplication, or rate limiting—why here?

---

## W. Security & compliance (expanded)

179. Did you participate in audits or pen tests—what findings did you remediate?
180. Did you implement authn/z changes (SSO, OAuth, RBAC, ABAC)—scope?
181. Did you handle secrets rotation, KMS, or vault usage—what improved?
182. Did you work on data residency or cross-border transfers—constraints?

---

## X. Product sense & UX (for eng roles with product overlap)

183. What user research did you consume or contribute to?
184. What UX problems did you identify from data or support tickets—what did you ship?
185. Did you propose scope changes based on user value—example?

---

## Y. Management & leadership (if applicable)

186. Team size you directly supported (people management or tech lead scope).
187. How did you set goals for others—cadence and measurement?
188. How did you handle underperformance or interpersonal issues (high level)?
189. Did you run performance calibrations or growth plans—your philosophy in one paragraph?
190. Hiring: how many hires did you drive—what bar did you optimize for?

---

## Z. Narrative arcs & interview stories (STAR prep as data)

191. Story 1: Situation (context), Task (your job), Action (what you did), Result (outcome + metric).
192. Story 2: STAR (different domain than Story 1—e.g. conflict vs technical).
193. Story 3: STAR (failure or setback with recovery).
194. Story 4: STAR (mentorship, inclusion, or cross-team alignment).
195. Story 5: STAR (incident or crisis response).

---

## AA. Job-specific keyword honesty grid (optional)

For each keyword you might want on a tailored resume, answer **where you used it** and **how deep** (read docs / shipped small / shipped large / owned production).

196. Keyword: ______ — depth and proof.
197. Keyword: ______ — depth and proof.
198. Keyword: ______ — depth and proof.
199. Keyword: ______ — depth and proof.
200. Keyword: ______ — depth and proof.

---

## AB. References & verification (private; optional for your own notes)

201. Colleagues who could speak to your work (roles only—do not export names to public JSON if you prefer).
202. Artifacts you could show in a portfolio (redacted screenshots, diagrams)—list availability.

---

## Using this file with JSON export

- Each numbered item can become one `{ "question": "…", "answer": "…" }` entry.
- For **repeatable** blocks (projects), either prefix the question with the project name in the string, e.g. `"Project Aurora — What was the hardest technical challenge?"`, or put each project in a **separate file** and link it with **`projectRefs`** on the job export — see **`examples/LINKED_PROJECTS.md`** and **`schemas/resume-project-fragment.schema.json`**. (A v2 structured schema is also possible.)
- Sections **T–AB** are optional modules—include in export only when filled.
- Empty answers may be omitted when exporting to keep token count down.
