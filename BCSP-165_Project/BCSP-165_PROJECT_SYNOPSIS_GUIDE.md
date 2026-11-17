# IGNOU BCA (NEW) — BCSP-165 Project Synopsis Guide
*Compiled for a BCA_NEW Semester 5 student preparing to submit the synopsis so the project can be done in Semester 6. Researched Nov 2026.*

---

## 1. What this course actually is

| Fact | Detail |
|---|---|
| Course code | **BCSP-165** (BCA_NEW and BCA_NEWOL). The OLD syllabus used BCSP-064 — don't mix the two. |
| Credits | 12 (this is why the evaluation fee is higher) |
| Semester | VI |
| Who can do it | **One student per project** — group projects are NOT allowed |
| Marks | Report: **150** + Viva-voce: **50** (you must get at least ~50% in each separately) |
| Evaluation fee | ~Rs 500 (paid with the Term-End Exam form; confirm the amount on the form) |
| Viva | Includes a **compulsory live coding demonstration** — your code WILL be run |

⚠️ Your guide may guide **at most 8** BCA_NEW/BCA_NEWOL learners at any time (you included).

---

## 2. The official IGNOU documents (download these)

1. **BCSP-165 Project Guidelines (SOCIS, 77 pages — THE rulebook)**
   - eGyanKosh page: https://egyankosh.ac.in/handle/123456789/123879
   - Direct PDF ("View/Open"): usually `https://egyankosh.ac.in/bitstream/123456789/123879/1/BCSP-165.pdf`
   - Key page numbers inside it: calendar p.58, proposal proforma p.59, proposal checklist p.60, synopsis contents p.61, report contents p.63, tools list p.66, Certificate of Originality p.70, sample title page p.72, Annexures 1–3 pp.73–76.
2. **BCA_NEW Programme Guide v2.0 (July 2026)**
   - https://www.ignou.ac.in/viewFile/SOCIS/programmeguide/BCA_NEW-May-2026.pdf
3. **Old-syllabus BCSP-064 guidelines** (only if your registration shows BCSP-064):
   - https://webservices.ignou.ac.in/assignments/Bachelor-Degree/BCA/2023-24/BCSP064_Project_Guidelines%20July%202023-Jan%202024.pdf

---

## 3. How many pages should the synopsis be?

**12 to 15 pages.** This is the official length from the BCSP-165 guidelines (checked on the p.60 checklist and enforced by evaluators). Shorter or longer risks a "summarily rejected" proposal.

---

## 4. What goes inside the synopsis (Section III + Annexure-2)

### Front matter (not counted in your chapter numbering)
- **Title page** (use the format printed on p.72 of the guidelines)
- **The original Proforma** — the printed proforma, filled, **signed AND dated by you and your guide** (a photocopy is not accepted)
- **Certificate of Authentication of Work** (signed by you and your guide)
- Abstract (a short summary of the whole project)
- Acknowledgement
- Table of Contents

### Chapter 1 — Introduction
- 1.1 Background
- 1.2 Objectives
- 1.3 Purpose, Scope and Applicability
- 1.4 Software and Hardware Technologies (tools/platforms you will use)
- Also add here: **Project Category** (RDBMS / OOPS / Networking / Multimedia / AI / Expert Systems) and whether there is an **industry/client** (Yes/No; if yes, name and address)

### Chapter 2 — Requirements & Analysis (the heavy part)
- 2.1 Problem Definition
- 2.2 Requirements Specification
- 2.3 Conceptual Models:
  - **DFDs up to at least the SECOND level** (Level 1 + a Level 2 DFD for *every* Level 1 process)
  - **ER diagram** (or class diagram for OOP projects)

### Chapter 3 — Basic System Design
- 3.1 Basic Modules
- 3.2 Database Design (tables, fields, keys, constraints)
- 3.3 Procedural Design (process logic, flowcharts/algorithm sketches)
- 3.6 Test Cases Design (yes, even in the synopsis)

### End matter
- Future Scope and Further Enhancement (add after 3.6)

### ⚠️ The mapping rule most students miss (footnotes of Annexure-2)
Everything must tell the SAME story:
1. **ER entities ↔ DFD data stores ↔ database tables** must map to each other by name.
2. **Number of modules = number of Level 1 DFD processes**, paired in the same order.
3. **Every Level 1 process must have a Level 2 diagram.**

Cleanest trick: pick the same number of modules as Level-1 processes, data stores, entities and tables (e.g. 6 of each) and keep the names consistent.

---

## 5. The proposal package — what goes in the envelope

Send to the **Regional Director of YOUR Regional Centre** (NOT to SOCIS Delhi — a common mistake):

1. Proforma (p.59 of guidelines), filled, signed and **dated** by both you and the guide
2. Guide's **bio-data, signed and dated by the guide** (include degrees — must be in Computer Science/IT — designation, organisation, address, years of experience)
3. The synopsis (12–15 pages)
4. A **self-addressed envelope with postage stamps** (the decision comes by post)

Keep a photocopy of the whole package.

### Guide eligibility (Section IV)
| Route | Qualification | Experience |
|---|---|---|
| 1 | Ph.D. or M.Tech. in Computer Science | none required |
| 2 | B.E./B.Tech. (CS), MCA, or M.Sc. (CS) | at least 2 years (industry or teaching) |

Every degree must be in **Computer Science / IT only**.

---

## 6. Calendar — two proposal slots per year

| You send the synopsis to the Regional Director | Approval decision | Report window (1 hard-bound copy) | Viva |
|---|---|---|---|
| 1 April – 30 June | ~30 days | 1 July – 30 Sept | January |
| 1 October – 31 December | ~30 days | 1 Jan – 31 March | July |

- If rejected, you can resubmit **only in the next slot** → 6 months lost. Get it right the first time.
- If not approved, you receive "Suggestions for reformulating the project" — you MUST implement those comments in the report later.

---

## 7. The project report (for later — plan for it now)

- About **100 double-spaced A4 pages, code excluded** (10% either way → aim 90–110)
- A4, double spacing, **hard bound** (spiral binding NOT permitted; no photocopies)
- Times New Roman 12pt, 2-inch left margin, 1-inch elsewhere
- Must bind in: original approved proforma, signed synopsis, signed bio-data, Certificate of Originality
- Chapters (Annexure-3): Introduction → Requirements & Analysis → System Design → Implementation & Testing (unit/integration/system tests kept **separate**) → Results & Discussion → Conclusions + references/glossary/appendix with **complete code**
- Top of envelope: **"BCA_NEW/BCA_NEWOL PROJECT REPORT (BCSP-165)"**, sent by registered insured post to the Regional Director
- Keep one identical copy for the viva

---

## 8. Example synopses available online

- **Sample BCSP-165 synopsis (21 pages, follows Annexure-2 heading by heading)** — topic: lab slot booking & practical attendance tracker:
  https://ignouproject.com/wp-content/uploads/2026/10/ignou-bca-bcsp-165-sample-synopsis.pdf
- **Empty report-format template (Annexure-3 chapter by chapter)**:
  https://ignouproject.com/wp-content/uploads/2026/10/ignou-bca-bcsp-165-project-report-format.pdf
- **Full explainer page** (where most of this summary comes from, with source citations):
  https://ignouproject.com/ignou-bca-project-bcsp-165
- Many paid "ready-made" synopsis sellers exist. ⚠️ **Section V of the guidelines warns that copied synopses get very low scores and can be sent to IGNOU's Unfair Means Committee.** Use examples only to learn the FORMAT — write your own content.

---

## 9. Topic guidance

IGNOU publishes no topic list. Rules: it must **compulsorily include software development**, be complex enough to justify a BCA project, and preferably solve a real problem for a real organisation. Good sources of ideas: your own Sem-5/6 electives (BCOS-184 E-Commerce, BECS-184 Data Analysis, MSEI-023 Cyber Security, etc.) plus MCS-207 (DBMS) and BCS-053 (Web Programming).

⚠️ If you plan to do IGNOU MCA later: MCSP-232 rules say don't repeat your BCA topic.

⚠️ The title written on the proforma **locks the report title word-for-word** — a different title gets the report returned.

---

## 10. Quick checklist before you post the synopsis

- [ ] Title decided (final — it locks)
- [ ] Guide found, eligibility verified, bio-data signed & dated
- [ ] Synopsis 12–15 pages
- [ ] Level 1 DFD + Level 2 DFD for every Level 1 process
- [ ] ER diagram + database design
- [ ] Entities = data stores = tables (mapped by name)
- [ ] Modules count = Level 1 processes count
- [ ] Test cases section included
- [ ] Proforma: every box filled, both signatures dated
- [ ] Self-addressed stamped envelope included
- [ ] Addressed to Regional Director, keep a photocopy
