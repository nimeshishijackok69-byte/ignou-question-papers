# BCSP-165 Project Blueprint — FormFlow
*Project selected from GitHub: github.com/nimeshishijackok69-byte/work ("FormFlow" — multi-layer form & review management system)*

---

## 1. Proposed title (locks word-for-word on the proforma — decide carefully)

**"Web-Based Multi-Layer Form and Review Management System"**

(Alternatives: "Design and Development of a Web-Based Form and Review Management System for Educational Institutions")

Category: RDBMS + Web Application. Industry/client: answer honestly (Yes → name the school/organisation that used it, with address; No → say personal/academic development).

## 2. Tool stack for proforma item 6 and synopsis §1.4

Next.js 14 (TypeScript), PostgreSQL (Supabase) with Row-Level Security, NextAuth v5, Resend (email),
Tailwind CSS + shadcn/ui, React Hook Form + Zod, Zustand, Recharts, Vitest + Playwright, Vercel (hosting).

## 3. Mapping table (Annexure-2 rule: modules = Level-1 processes; entities = data stores = tables)

| Module | Level-1 DFD process | Data store | Database table(s) |
|---|---|---|---|
| M1. Event & Form Builder Management | 1.0 Manage Events and Forms | D1 Event | event_master, admin_profile |
| M2. Public Form Filling (Teacher) | 2.0 Register and Fill Form | D2 Respondent | user_master |
| M3. Submission Processing | 3.0 Process Submission | D3 Submission | submission |
| M4. Review Assignment & Multi-Layer Evaluation | 4.0 Assign and Conduct Review | D4 Review | review_assignment, review, reviewer_master |
| M5. Notification & Email Service | 5.0 Send Notifications | D5 Notification | notification |
| M6. Audit Trail & Analytics | 6.0 Log and Report | D6 Transaction | transaction_master |

ER entities: ADMIN, EVENT, RESPONDENT, SUBMISSION, REVIEWER, REVIEW_ASSIGNMENT, REVIEW, NOTIFICATION, TRANSACTION
(9 entities ↔ 9 tables; data stores can group these into D1–D6 above — keep names consistent everywhere.)

Level-2 DFDs needed for: each of processes 1.0–6.0 (six diagrams).
Security section (synopsis + report): cover RLS policies, NextAuth sessions, draft-token access, file-upload restrictions,
and (guidelines requirement) how passwords are stored/protected in transmission (bcrypt, HTTPS).

## 4. Synopsis skeleton (12–15 pages total)

- Title page (format p.72 of BCSP-165 guidelines)
- Original proforma (signed + dated by you and guide)
- Certificate of Authentication of Work
- Abstract (~1 page)
- Acknowledgement + Table of Contents
- Ch.1 Introduction: background, objectives, purpose/scope, software & hardware technologies, project category, client Y/N  (~2 pp)
- Ch.2 Analysis: problem definition, requirements, Level-0/1 DFD, six Level-2 DFDs, ER diagram  (~4–5 pp)
- Ch.3 Design: 6 modules, database design (9 tables with fields/keys/RLS summary), procedural design notes, test case design  (~4–5 pp)
- Future scope  (~½ p)

## 5. Test design material (already exists in the repo)

- Unit tests: tests/unit/ (Zod schemas, form-schema normaliser, rate limiter, env validator) → **unit test design**
- E2E: tests/e2e/ Playwright → **integration/system test design**
- Report §4.3 needs unit / integration / system tests kept SEPARATE with debug details.

## 6. Repo cleanup before anything official links to it

- [ ] Delete: CLAUDE.md, AGENTS.md, .ai/, handoff_context.txt, log.md, bug.md, scratch_test.ts, supabase*debug*.log, supabase_start.log, check_supabase.js
- [ ] Sanity-check README (remove "30,000+ schools" claim unless true; keep it factual)
- [ ] Confirm the app builds and runs locally (npm run dev) and the Vercel deployment is alive

## 7. Viva prep (50 marks, live coding demo compulsory)

- Walk the Level-1 DFD → show which module implements each process
- Open Supabase tables → name the ER entity / data store each maps to
- Run one passing and one failing test case live
- Explain the share-slug trigger function or fn_log_transaction (good algorithm to explain)
- Explain password storage (bcrypt) and HTTPS transport protection
- Be ready to explain JSONB form_schema, RLS policies, NextAuth session flow, draft_token mechanism

## 8. Timeline (today = 14 Nov 2026)

- NOW → mid-Dec 2026: finish synopsis + proforma + guide bio-data → post to Regional Director (Oct 1–31 Dec slot)
- ~4 weeks: approval by post
- 1 Jan – 31 Mar 2027: write & bind report (~100 double-spaced A4 pages, code excluded), post 1 hard-bound copy + guide remuneration form (separate envelope), envelope marked "BCA_NEW/BCA_NEWOL PROJECT REPORT (BCSP-165)", Rs 500 fee with TEE form
- July 2027: viva

## 9. Before starting

- [ ] Guide confirmed (CS/IT degree; B.Tech/MCA/M.Sc-CS route needs ≥2 yrs experience; ≤8 students total)
- [ ] Decide title — it cannot change later without the report being returned
- [ ] If planning IGNOU MCA later: pick a DIFFERENT topic there (MCSP-232 rule)
