# Repository Guidelines

## Project Structure & Module Organization

This repository is a static GitHub Pages personal website. Core pages live at the repository root:

- `index.html`: homepage and profile bio.
- `research.html`: research, papers, and reports.
- `projects.html`: OECD consulting and GitHub project summaries.
- `styles.css`: shared site styling.
- `Resume_CV_.pdf`: public CV linked from the navigation.
- `assets/`: profile image and ignored local QA screenshots.

Keep new public assets in `assets/`. Do not commit private contract drafts, background notes, or temporary browser screenshots; `.gitignore` already excludes known private OECD files and `assets/check-*.png`.

## Build, Test, and Development Commands

No build step is required. The site can be opened directly in a browser:

```powershell
start index.html
```

Useful checks before publishing:

```powershell
git status --short
git diff --check
```

`git diff --check` catches whitespace issues. For visual QA, open `index.html`, `research.html`, and `projects.html` locally, or capture a browser screenshot of the relevant page.

## Coding Style & Naming Conventions

Use plain HTML and CSS. Keep indentation at two spaces in HTML, match the existing serif academic design, and avoid unnecessary JavaScript or build tooling. File names should remain simple and stable because GitHub Pages serves them directly. Keep internal links relative, for example `projects.html` and `Resume_CV_.pdf`.

When editing content, use concise academic prose. Research entries should keep citation-style formatting; project descriptions should be based on the linked repository documentation or source materials.

## Testing Guidelines

There is no automated test suite. Validate changes manually by checking:

- Local links resolve for `index.html`, `research.html`, and `projects.html`.
- The CV link opens `Resume_CV_.pdf`.
- Long headings and project descriptions wrap cleanly on desktop and mobile.
- No private documents appear in `git status --short`.

## Commit & Pull Request Guidelines

Recent commits use short imperative messages, for example `Update CV PDF`, `Split OECD consultancy projects`, and `Update AI exposure project summary`. Follow that pattern.

For pull requests, include a brief description of changed pages, note whether `Resume_CV_.pdf` changed, and attach screenshots for visible layout changes. If adding project descriptions, mention the documentation source used.

## Security & Privacy

This is a public repository. Never commit private consultancy contracts, draft background notes, local caches, or unpublished source documents. If a private file is used to update public text, summarize it generally and ensure the file remains ignored and untracked.
