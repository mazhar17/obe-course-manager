# OBE Course Manager

A free, single-file web app for managing **teaching, learning & assessment from the OBE (Outcome-Based Education) perspective** — built for engineering faculty working under the Washington Accord / BAETE framework.

Everything runs in the browser. No server, no database, no login. All data stays on the user's device (browser localStorage), with JSON/CSV export–import for backup and sharing.

## Features

- **Course Info** — course code, title, credits, semester, program, teacher; editable attainment thresholds.
- **COs & CO–PO Mapping** — write CO statements with Bloom's taxonomy levels; click-to-set CO–PO mapping matrix (correlation strengths 1/2/3) against the 12 Washington Accord Program Outcomes.
- **Assessments** — plan quizzes, class tests, mid/final exams, labs, projects; every item/question is tagged with a CO and maximum marks.
- **Students & Marks** — add students individually or bulk-paste from Excel; spreadsheet-style marks grid; CSV export/import of the full marks sheet.
- **Attainment** — automatic CO attainment (% of students scoring above the threshold per CO) and PO attainment (weighted by mapping strength), with color-coded tables and charts against the target line.
- **Course Report** — printable OBE course report (course info, COs, CO–PO matrix, assessment plan, CO/PO attainment, CQI remarks, signature blocks). Use *Print → Save as PDF* for accreditation evidence.
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

- Data is stored **per browser, per device** (localStorage). Clearing browser data erases it — export a JSON backup regularly from **Data & Backup**.
- To move to another device or share with the department, export JSON and import it there.
- Nothing is ever uploaded anywhere; the app has no backend.

## Attainment method (default, editable per course)

- A student **attains a CO** if they score ≥ **60%** of the marks assessed under that CO.
- **CO attainment** = percentage of assessed students who attained the CO.
  - Level 3 (Excellent): ≥ 80% of students · Level 2 (Good): ≥ 70% · Level 1 (Satisfactory, target): ≥ 60%.
- **PO attainment** (course contribution) = weighted average of CO attainments, weighted by CO–PO correlation strengths (1–3).

All thresholds can be changed in **Course Info → Attainment Settings**.
