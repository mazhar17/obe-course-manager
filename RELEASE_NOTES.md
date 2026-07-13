# OBE Course Manager — Release Notes

Version: v1.4
First release: July 13, 2026
Live at: https://mazhar17.github.io/obe-course-manager/
License: © 2026 Prof. Mazharul Islam
Creative Commons Attribution (CC BY) 4.0 International

---

## Highlights

OBE Course Manager is a free tool for managing a course from the Outcome-Based Education (OBE) perspective, in line with the requirements of the Board of Accreditation for Engineering and Technical Education (BAETE) under the Washington Accord framework. It takes a course teacher through the complete OBE cycle — from writing Course Outcomes to printing signed accreditation evidence — and closes the Continuous Quality Improvement (CQI) loop between semesters. The underlying OBE implementation framework was developed at Ahsanullah University of Science and Technology (AUST) in early 2018 by Prof. Mazharul Islam along with his team from AUST. 

The entire application is a single, self-contained HTML file that runs in any modern browser — no installation, no account, no server. All data stays on the user's own device, with the option of working directly on a file for cloud-backed safety.

## Key Features

- Course setup — course information (including cohort), Course Outcomes with Bloom's taxonomy levels (cognitive, affective, psychomotor), and a click-to-set CO–PO mapping matrix against the 12 Washington Accord Program Outcomes.
- T&L Activities recommender (CQI-aware) — a pool of 31 evidence-based teaching-learning activities, matched to each CO's Bloom's level, boosted by the previous semester's CQI recommendations and ranked down when marked ineffective; one-click adoption into the constructive-alignment table. The pool is extensible.
- Assessment planning — quizzes, tests, exams, labs and projects broken into items, each tagged with a CO and maximum marks; the tagging drives all attainment calculations.
- Marks management — spreadsheet-style entry, bulk student paste from Excel, and a CSV workflow (Empty Template → Import → Export).
- Direct measurement of COs & POs — identical to the AUST Direct CO-PO Calculations method: per-student CO scores, % of students above the Target Pass Marks and KPI thresholds, and marks-weighted PO scores, with charts.
- Indirect measurement — a printable CO Exit Survey (or Google Forms + CSV import), with Likert-based indirect attainment per CO and PO.
- Combined attainment — direct and indirect results combined with user-editable weights (default 80/20).
- CQI tab (BAETE Criteria 3.8 & 5.4.3) — teaching-learning and assessment narratives, a six-step CQI-loop status board, low-attainment analysis (filter weak students per CO, item-wise diagnostics, analyses w.r.t. T&L activities and assessment techniques), a stakeholder feedback register, and an Annexure H evidence checklist — all two-way linked with the Course Specifications and Course Report.
- "Duplicate for New Semester" — carries CQI action plans from the Course Report into the next offering's Course Specifications automatically, closing the loop.
- Data safety — work directly on a `.json` file with auto-save (Chrome/Edge), keep it in a cloud-synced folder, exchange it with colleagues; JSON export/import for backups and sharing.

## Accreditation Documents Produced

All auto-filled from the course data, editable in place, and printable to PDF:

1. Course Outline — with CO–PO/Bloom's mapping, Knowledge Profile / Complex Problem / Complex Activities mapping, assessment percentages, and the 14-week plan
2. Course Specifications — SLT, constructive alignment, planned contact hours, assessment blueprint, CQI measures
3. Final Examination Vetting Form — CO–question matrix auto-filled for moderation
4. Direct Measurements of COs & POs — the attainment report, computed automatically
5. CO Exit Survey — the indirect-measurement instrument
6. Course Report — attainment results, grade distribution, resources and TLA analysis, CQI action plans
7. CQI Report — consolidated BAETE 3.8 / 5.4.3 evidence for Annexure H

## Getting Started

Open https://mazhar17.github.io/obe-course-manager/ in Chrome or Edge, click Load Sample Course on the Dashboard to explore, then create your own course. A detailed Faculty User Manual accompanies this release; see `change_log.txt` for the version history.
