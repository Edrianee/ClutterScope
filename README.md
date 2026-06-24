# ClutterScope — UI Mockup

Interactive UI mockup for **ClutterScope: A Digital Clutter Score Analyzer for Windows-Based Personal Computers**, a capstone project for the course Quantitative Methods (ITQM).

ClutterScope is a Windows desktop application (Python / PySide6) that scans selected folders and computes a **0–100 clutter score** based on four indicators:

- **Duplicate files** (detected via SHA-256 hash comparison)
- **Improperly named files** (deviating from naming conventions)
- **Excessive folder depth** (directories nested beyond 5 levels)
- **Unused files** (not accessed or modified in over 12 months)

## Live mockup

👉 **https://YOUR-USERNAME.github.io/clutterscope/**

_(Replace `YOUR-USERNAME` with your GitHub username once GitHub Pages is enabled.)_

## Screens

The mockup shows the four screens defined in Chapter 2:

1. **Home** — folder selector and Start Scan button
2. **Scanning** — progress indicator and file/folder counters
3. **Results Dashboard** — circular score gauge, interpretation band, issue breakdown, recoverable storage
4. **Recommendations & Report** — advisory corrective actions and PDF/CSV export

## How to run locally

Just open `index.html` in any web browser. It is a single self-contained file with no dependencies.

## Authors

- Ronald Justin Baldo
- Giancarlo Capilitan
- Jhan Edrian Panado

June 2026
