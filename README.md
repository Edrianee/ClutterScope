# ClutterScope — UI Mockup

Interactive UI mockup for **ClutterScope**, a clutter and file findability scoring tool with machine learning-based retrieval risk prediction. ClutterScope is a Windows desktop application (Python / PySide6, scikit-learn, SQLite).

ClutterScope reads file **metadata only** and computes:

- a **findability score** (0–100) per file — filename descriptiveness, distinguishing terms, name collisions, path context
- a **clutter score** (0–100, higher = more cluttered) per folder — duplicate files (SHA-256), folder depth beyond 5 levels, unused files (12+ months), and the findability of contained files
- a **retrieval risk** per file — *Findable*, *Uncertain* or *Likely Lost*, with a confidence value (ML classifier)

Recommendations (**rename, archive, delete, keep**) are mapped from risk and indicators by fixed rules. Every action needs confirmation, deletions go to the Recycle Bin, and all actions are logged with undo.

> Scoring weights and thresholds in the mockup are **placeholders**. Files, scores and predictions are simulated.

## Live mockup

👉 **https://edrianee.github.io/ClutterScope/**

_(Available once GitHub Pages is enabled for this repository.)_

## Pages

1. **Dashboard** — files scanned, average findability, at-risk files, duplicates, unused files, recommended actions, risk distribution, most cluttered folders
2. **Scan** — folder selection (system folders blocked), progress through the processing steps, results summary
3. **File Analysis** — per-file findability, risk, indicators and explanation; per-folder clutter scores
4. **Recommendations** — by default (*Review & apply*), every recommended rename, archive, delete and keep action is listed per file with its reason and safety rating; each file can be unticked and each suggested name edited, and the selected actions are applied in one confirmed step (undoable as a batch). With *Manual review* (Settings), each suggested filename is confirmed or cancelled individually, and duplicate groups and unused files are selected and archived or deleted to the Recycle Bin
5. **Action History** — original/new filename, date and time, status, per-row undo
6. **Reports** — Findability, Retrieval-Risk, Clutter and Action reports; CSV and PDF export

Plus **Settings** (theme, *Review & apply* or *Manual review* recommendations, locked safety rules, scoring rules). The mockup shows only what users of the released app will see. The retrieval trials that train the classifier run on a separate web page.

See [CHANGELOG.md](CHANGELOG.md) for what changed in each version.

## How to run locally

Open `index.html` in any web browser. It is a single self-contained file with no dependencies.

## Authors

- Ronald Justin Baldo
- Alma May Monterozo
- Jhan Edrian Panado

2026
