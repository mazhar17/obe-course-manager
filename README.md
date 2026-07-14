# OBE Course Manager — v1.9 (First release: July 13, 2026)

See `change_log.txt` for the version history.

A free, single-file web app for managing **teaching, learning & assessment from the OBE (Outcome-Based Education) perspective** — built for engineering faculty working under the Washington Accord / BAETE framework.

Everything runs in the browser. No server, no database, no login. All data stays on the user's device (browser localStorage), with JSON/CSV export–import for backup and sharing.

## Features

- **Course Info** — course code, title, credits, semester, program, teacher; editable attainment thresholds.
- **COs & CO–PO Mapping** — write CO statements with Bloom's taxonomy levels; click-to-set CO–PO mapping matrix (correlation strengths 1/2/3) against the 12 Washington Accord Program Outcomes.
- **T&L Activities (CQI recommender)** — a built-in pool of 31 teaching & learning activities tagged by Bloom's level, mode (in-person/online), and class size. For each CO the app recommends the best-fitting activities, **boosting** ones suggested in the previous semester's CQI recommendations (Course Specifications 6.1 / Course Report 6.1) and **ranking down** ones marked ineffective in the previous Course Report (3.2). One click adopts an activity into the CO's delivery methods, which then flow automatically into the Course Specifications constructive-alignment table — closing the CQI loop. Faculty/departments can extend the pool with custom activities (kept in backups for sharing).
- **Assessments** — plan quizzes, class tests, mid/final exams, labs, projects; every item/question is tagged with a CO and maximum marks.
- **Students & Marks** — add students individually or bulk-paste from Excel; spreadsheet-style marks grid; CSV export/import of the full marks sheet.
- **Attainment (Direct)** — automatic CO attainment (% of students scoring above the threshold per CO) and PO attainment (weighted by mapping strength), with color-coded tables and charts against the target line.
- **Indirect Measurement (CO Exit Survey)** — students rate each CO on a 5-point Likert scale at semester end. Enter response counts in a tally grid, or import the CSV from a Google Form (one column per CO). Indirect CO attainment = % of responses rated at/above the threshold (default ≥ 4); indirect PO values are derived through the CO–PO mapping, weighted by CO marks. A printable survey form is included under Accreditation Documents, and the results feed Course Report section 5.1 automatically.
- **Combined Attainment** — weighted combination of direct and indirect measurements (default 80/20, editable), per CO and PO, judged against the same Target KPI.
- **CQI tab (BAETE Criteria 3.8 & 5.4.3)** — an auto-compiled per-CO table of T&L methods, assessment tools and complex-problem (CP/CEA) coverage; narrative fields for how methods address complex engineering problems, their effectiveness, assessment-tool design, and question moderation; a live six-step CQI-loop status board; improvement-action tables two-way linked with Course Report 6.1 and Course Specifications 6.1; a **Low Attainment Analysis** linked to the Attainment tab (filter students below a threshold per CO, see item-wise average scores with weak items highlighted, and record analyses w.r.t. T&L activities and assessment techniques plus comments); a stakeholder feedback register; and an Annexure H evidence checklist. A consolidated printable **CQI Report** is included under Accreditation Documents.
- **Accreditation Documents** — the standard OBE documents (following the AUST templates), auto-filled from the course data and printable (*Print → Save as PDF*):
  1. **Course Outline** (COs with PO/Bloom C-A-P mapping, Knowledge Profile / Complex Problem / Complex Activities mapping, assessment method percentages, 14-week plan, references, signature blocks)
  2. **Course Specifications** (SLT, constructive alignment table, planned contact hours, assessment blueprint, CQI recommendations)
  3. **Final Examination Vetting Form** (CO–question mapping auto-filled per assessment, checklist, vetter verification and signature blocks)
  4. **Direct CO-PO Calculations** (same method and layout as the AUST workbook: % of students above Target Pass Marks and above KPI, per CO and PO)
  5. **Course Report** (CO analysis with modification columns, contact-hour variation, TLA and resources analysis, IUMS grade distribution, CO/PO KPI attainment, indirect assessment, CQI action plans, HOD approval)

  Dotted fields in these documents are editable in place and save automatically; everything already entered elsewhere in the app fills in by itself.
- **Data & Backup** — export/import all courses or a single course as JSON; share a course file with a colleague or the OBE committee.
- Multiple courses are supported — switch from the dropdown in the header.
- A built-in **sample course** (Dashboard → *Load Sample Course*) lets you explore every feature instantly.

## How to host on GitHub Pages (free)

1. Sign in at [github.com](https://github.com) (create a free account if needed).
2. Click **+** (top right) → **New repository**. Name it e.g. `obe-course-manager`, keep it **Public**, click **Create repository**.
3. On the repository page, click **uploading an existing file**, drag in `index.html` (and this `README.md`), then click **Commit changes**.
4. Go to **Settings → Pages** (left sidebar).
5. Under **Build and deployment → Source**, choose **Deploy from a branch**; select branch **main** and folder **/ (root)**; click **Save**.
6. Wait ~1 minute. Your app will be live at:
   `https://<your-username>.github.io/obe-course-manager/`

Share that link with colleagues — each person's data stays private in their own browser.

### Updating the app later
Edit or re-upload `index.html` in the repository (Add file → Upload files → Commit). GitHub Pages redeploys automatically.

## Running without hosting

Just double-click `index.html` — it opens and works in any modern browser (Chrome, Edge, Firefox). Internet is needed only on first load, for the chart library.

## Important notes on data

- **Recommended: work on a real file.** In Chrome/Edge, use **Data & Backup → Save As New File…** (or the 💾 button in the header) to keep all data in a `.json` file on your computer. Every change then auto-saves to the file (header shows "saved"/"saving…"). Keep the file in a OneDrive/Google Drive/Dropbox folder and it is backed up and portable across computers. After reopening the browser, click **Reconnect** once to resume.
- Without a linked file, data is stored per browser, per device (localStorage) — clearing browser data erases it, so export JSON backups regularly from **Data & Backup**.
- To share with the department, send the `.json` file (or a JSON export) — colleagues open it via **Open Data File…** or Import.
- Nothing is ever uploaded anywhere; the app has no backend.

## Attainment method (AUST Direct CO-PO Measurement)

Identical to the AUST "Direct CO-PO Calculations" workbook:

- A student's **CO score** = percentage obtained of the marks allocated to that CO (blank marks count as 0).
- **CO measurement** = % of students scoring **above the Target Pass Marks** (default 40); also reported: % of students above the KPI marks (default 50).
- A student's **PO score** = the student's CO scores mapped to that PO, weighted by each CO's allocated marks (any CO–PO mapping strength > 0 counts as mapped).
- A CO/PO is **attained** when the % of students above the pass marks reaches the **Target KPI** (default 50%).

All three thresholds are editable per course in **Course Info → Attainment Settings**.

## License

© 2026 Prof. Mazharul Islam. Distributed under the [Creative Commons Attribution (CC BY) 4.0 International License](https://creativecommons.org/licenses/by/4.0/) — free to share and adapt with attribution.
