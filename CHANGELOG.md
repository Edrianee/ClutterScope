# Changelog

All notable changes to the ClutterScope UI mockup.

## v2.1 — 2026-10-08

### Added
- **One-click apply** is now the default on the Recommendations page. A summary shows every recommended action grouped as delete, archive, rename and keep, with the expected effect on average findability, at-risk files, overall clutter and duplicate space. A single **Apply all recommendations** button applies them together.
- The confirmation dialog for one-click apply lists what each group will do, and **Apply** stays disabled until the user ticks *"I reviewed this summary…"*.
- Groups can be left out by unticking them, and each group has a "Show files" list (old → new names for renames, the original for each duplicate copy).
- Follow-up actions are planned in advance. For example, a file that becomes findable after a rename and is unused is also archived, so one click leaves no recommendations behind.
- The whole batch can be undone at once (Undo or Ctrl+Z). Each action still appears separately in Action History with its own undo.
- **Settings → Recommendations** switches between *One-click apply* and *Manual review*. The choice is remembered.

### Changed
- **Clutter Management is merged into Recommendations**, leaving six pages in the sidebar. In one-click mode, duplicate copies and unused files are part of the Delete and Archive groups. In Manual review, the duplicate groups (original vs. copies, SHA-256) and the unused-files list appear at the bottom of the page with their Archive / Delete to Recycle Bin bar.
- The Recommendations badge and the Dashboard's *Recommended actions* counts now match the actions that will be applied.
- The Help text, Action History empty message and README describe the new flow.

### Fixed
- The Recommendations badge now updates as soon as the recommendation mode changes.

## v2.0 — 2026-10-02

### Changed
- Rebuilt the mockup around per-file **findability scores**, per-folder **clutter scores** and a simulated **retrieval-risk prediction** (Findable / Uncertain / Likely Lost, with confidence).
- Pages: Dashboard, Scan, File Analysis, Recommendations, Clutter Management, Action History and Reports, plus Settings and a researcher-only Retrieval Testing module.
- Rule-based actions (rename, archive, delete, keep), each with a confirmation dialog, Recycle Bin deletion and per-row undo.
- Scores update automatically after every action. A finished scan continues to File Analysis.
- Reports (Findability, Retrieval-Risk, Clutter, Action) export to CSV and PDF.
- Removed in-page buttons that duplicated the sidebar menu, and the old duplicate mockup file.

## v1.0 — 2026-06-24 to 2026-07-01

- First interactive mockup: home, scanning, results dashboard, clean up and report screens with a sidebar workflow stepper.
