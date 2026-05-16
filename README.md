# Full SP Submission of Clark Rodriguez
The following SP Github repository contains files and folders relevant to the Special Problem submission of: 

| Field | Details |
| :--- | :--- |
| **Student Name** | Augustus Clark Raphael P. Rodriguez |
| **Student Number** | 2022-08338 |
| **Course** | BS Computer Science 
---
The repository has the following file-structure
```
📦attestation
 ┣ 📜ORI-Attestation-Form.docx
📦sp-journal (journal article) 
📦manual
 ┣ 📦images
 ┣ 📜DEVELOPMENT.md
 ┗ 📜HELP.md
📦sp-manuscript (SP Docs)
📦a-mmc (src)
📜README.md
```
## Description of the Directories/Files

### `sp-manuscript` (SP Documents)
This directory contains the full contents of the SP manuscript. Below is the respective file-tree for the manuscript repository. 

```
  sp-manuscript/
  ├── rodriguez_sp-manuscript.tex       # Main document entry point
  ├── rodriguez_sp-manuscript.pdf       # Compiled output
  ├── titlepage.tex                     # Title page
  ├── acceptancesheet.tex               # Approval/acceptance sheet
  ├── chapter1.tex                      # Introduction
  ├── chapter2.tex                      # Review of Related Literature
  ├── chapter3.tex                      # Theoretical Framework
  ├── chapter4.tex                      # Design and Implementation
  ├── chapter5.tex                      # Results
  ├── chapter6.tex                      # Discussions
  ├── chapter7.tex                      # Conclusion
  ├── chapter8.tex                      # Reccomendations
  ├── appx-devlog.tex                   # Appendix: Development log
  ├── appx-gforms.tex                   # Appendix: Google Forms data
  ├── appx-refinement.tex               # Appendix: Refinement details
  ├── appx-sourcecode.tex               # Appendix: Source code listings
  ├── appx-ueq-qual.tex                 # Appendix: UEQ qualitative data
  ├── biblio.bib                        # BibTeX bibliography (IEEE style)
  ├── Rodriguez-SP-Proposal.tex         # Original SP proposal source
  ├── Rodriguez-SP-Proposal.pdf         # SP proposal compiled
  ├── RODRIGUEZ_DEFENSE.pptx            # Defense presentation
  ├── RODRIGUEZ_DEFENSE_APPX.pptx       # Defense appendix slides
  ├── images/
  │   ├── ch-3/                         # TF figures 
  │   ├── ch-4/                         # Design artifacts 
  │   └── ch-5/                         # Implementation figures
  │       ├── Low-Fidelity Prototype v1/     # Lo-fi prototype screens 
  │       ├── admin-scs/                     # Admin portal screenshots
  │       ├── doc-scs/                       # Clinician/doctor view screenshots
  │       ├── kiosk-scs/                     # Kiosk interface screenshots
  │       ├── patient-scs/                   # Patient view screenshots
  │       │   └── guided-search/             # Triage screenshots       
  │       ├── post-sret-wk-1/                # Post-SRET week 1 screenshots
  │       └── ueq/                           # UEQ result plots and benchmarks
  ├── source-code/                      # Discrete source-code files
  └── rgao-reb/                         # Ethics board documents
```

The directory is a module binding the respective repository of the SP manuscript to this one via: 
```bash
git submodule add https://github.com/krispybataa/sp-manuscript sp-manuscript
```
### `sp-journal` (Journal Article)
This 

The directory is a module binding the respective repository of the Journal Article to this one via: 
```bash
git submodule add https://github.com/krispybataa/sp-journal sp-journal
```
### `a-mmc` (Source Code)
This contains the full system source code of the system, bound via under the module a-mmc. The internal directory is as follows: 
```
a-mmc/
  ├── .github/workflows/          # CI pipelines for backend, frontend, kiosk
  ├── a-mmc_backend/
  │   ├── app/
  │   │   ├── models/             # SQLAlchemy models
  │   │   ├── routes/             # Flask blueprints, one per domain
  │   │   ├── services/           # System logic 
  │   │   └── utils/              # Shared helpers (validators)
  │   ├── config/                 # Environment configs 
  │   ├── data/                   # Seed scripts and clinician CSVs
  │   ├── migrations/             # Alembic migration files
  │   └── tests/                  # Pytest suite (services + validators)
  ├── a-mmc_frontend/
  │   ├── public/assets/          # Static images 
  │   └── src/
  │       ├── components/         # Shared UI Components
  │       ├── context/            # AuthContext 
  │       ├── data/               # triageLogic.js (Synced with Kiosk)
  │       ├── lib/                # Utility functions
  │       ├── pages/
  │       │   ├── admin/          # Admin Interfaces
  │       │   ├── dashboard/      # Patient and C/S dashboards
  │       │   ├── public/         # Public Interfaces
  │       │   └── staff/          # Staff login and clinician today view
  │       └── services/           # API client, PDF export, upload stub
  ├── a-mmc_infra/
  │   └── nginx/                  # Reverse proxy config and Dockerfile
  ├── a-mmc_kiosk/
  │   └── src/
  │       ├── components/         # Kiosk-specific UI 
  │       ├── data/               # triageLogic.js (Synced with main system)
  │       ├── pages/              # Kiosk screens
  │       └── services/           # API client
```
The directory is a module binding the respective repository of the SP manuscript to this one via: 
```bash
git submodule add https://github.com/krispybataa/a-mmc a-mmc
```
### `manual` (Manuals)
This directory simply contains the developer and user manuals for the SP system. Namely `DEVELOPMENT.md` and `HELP.md` respectively. 
### `attestation` (ORI Attestation)
This directory simply contains the UP-Manila ORI Attestation Document. 
### `README.md` 
This is the file descrbing the content of this repository and its internal sub-modules. 