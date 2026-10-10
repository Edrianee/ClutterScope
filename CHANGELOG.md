# Changelog

All notable changes to the ClutterScope UI mockup.

## v2.3 — 2026-10-10

### Changed
- **Review & apply** replaces one-click apply as the default on the Recommendations page. Every recommended action is now listed file by file with its rule and reason, and all are ticked by default.
  - Untick a file, or a whole group, to leave it out. The counts, the expected-effect tiles and the **Apply selected** button follow the selection.
  - Edit a suggested filename right in the list. The extension is kept, and a name that already exists in the folder is refused.
  - The selected actions are applied in one confirmed step and can still be undone as a batch.
- **Settings → Recommendations** now offers *Review & apply* or *Manual review*. The Help text, confirmation dialog and README use the new wording.
- Retrieval risk is presented as the classifier's prediction. The Dashboard legend no longer shows score cut-offs, and File Analysis labels it *Predicted retrieval risk*. Its note explains that the 70 / 45 score thresholds are only the rule-based baseline the classifier is compared against.
- Settings no longer names Random Forest. The classifier is chosen by comparing logistic regression, decision tree and random forest.

### Removed
- The researcher-only **Retrieval Testing** page and the *Researcher mode* switch in Settings. The retrieval trials now run on a separate web page, and the mockup shows only what users of the released app will see.

### Why
- A middle ground between one-click apply and fully manual review: users see and approve every action without confirming files one at a time.

## v2.2 — 2026-10-08

### Added
- **Safety ratings** for every action type: *Reversible · Recycle Bin* (delete), *Reversible · moved to archive* (archive), *Reversible · filename only* (rename) and *Safe · no change* (keep). They appear on the one-click plan, in the confirmation dialog and in Manual review.
- Each file in the one-click "Show files" lists now shows its **reason**: the rule (R1–R5) and why it applies.
- **Duplicate groups** table in the Clutter Report (SHA-256, original vs. copies, size), included in the CSV export.
- **Excluded-items log** on the Scan page. It lists each file or folder skipped by rule (system or hidden attribute, temporary file, no read permission) with the reason. The scan's *Excluded* counter now matches this list.
- Retrieval Testing uses its own **prepared sample folder set of 54 files**: 18 clear, 18 moderately ambiguous, and 18 generic or deeply nested. Each file has a task prompt and designed difficulty, and both are included in the labeled-dataset CSV.

### Changed
- The Settings "About" line no longer claims regulatory compliance. It now says all processing stays on the computer.
- Internal: per-file scoring is shared by the scanned files and the trial set.

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
