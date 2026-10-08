# ClutterScope â€” UI Mockup

Interactive UI mockup for **ClutterScope**, a clutter and file findability scoring tool with machine learning-based retrieval risk prediction. ClutterScope is a Windows desktop application (Python / PySide6, scikit-learn, SQLite).

ClutterScope reads file **metadata only** and computes:

- a **findability score** (0â€“100) per file â€” filename descriptiveness, distinguishing terms, name collisions, path context
- a **clutter score** (0â€“100, higher = more cluttered) per folder â€” duplicate files (SHA-256), folder depth beyond 5 levels, unused files (12+ months), and the findability of contained files
- a **retrieval risk** per file â€” *Findable*, *Uncertain* or *Likely Lost*, with a confidence value (ML classifier)

Recommendations (**rename, archive, delete, keep**) are mapped from risk and indicators by fixed rules. Every action needs confirmation, deletions go to the Recycle Bin, and all actions are logged with undo.

> Scoring weights and thresholds in the mockup are **placeholders**. Files, scores and predictions are simulated.

## Live mockup

ðŸ‘‰ **https://edrianee.github.io/ClutterScope/**

_(Available once GitHub Pages is enabled for this repository.)_

## Pages

1. **Dashboard** â€” files scanned, average findability, at-risk files, duplicates, unused files, recommended actions, risk distribution, most cluttered folders
2. **Scan** â€” folder selection (system folders blocked), progress through the processing steps, results summary
3. **File Analysis** â€” per-file findability, risk, indicators and explanation; per-folder clutter scores
4. **Recommendations** â€” by default, a summary of every recommended rename, archive, delete and keep action with its expected effect, applied in one confirmed step (undoable as a batch). With *Manual review* (Settings), each suggested filename is confirmed or cancelled individually, and duplicate groups and unused files are selected and archived or deleted to the Recycle Bin
5. **Action History** â€” original/new filename, date and time, status, per-row undo
6. **Reports** â€” Findability, Retrieval-Risk, Clutter and Action reports; CSV and PDF export

Plus **Settings** (theme, one-click or manual recommendations, locked safety rules, scoring rules) and a researcher-only **Retrieval Testing** module (enable *Researcher mode* in Settings) for collecting ground-truth retrieval outcomes.

See [CHANGELOG.md](CHANGELOG.md) for what changed in each version.

## How to run locally

Open `index.html` in any web browser. It is a single self-contained file with no dependencies.

## Authors

- Ronald Justin Baldo
- Alma May Monterozo
- Jhan Edrian Panado

2026
