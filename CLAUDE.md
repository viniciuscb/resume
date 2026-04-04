# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Structure

This is Vinicius Cubas Brand's resume repository with three parallel formats:

- `resume.tex` — English LaTeX version (primary source of truth)
- `pt-br/resume.tex` — Portuguese (Brazilian) translation
- `html/index.html` + `html/style.css` — Browser-viewable HTML/CSS version

## Building

**LaTeX → PDF:**
```bash
pdflatex resume.tex        # English
cd pt-br && pdflatex resume.tex   # Portuguese
```

**HTML version:** Open `html/index.html` directly in a browser. Print to PDF using browser print (Ctrl+P → Save as PDF).

## Content Sync Rules

All three versions must stay in sync when content changes. The English `.tex` is the canonical source; changes propagate to `pt-br/resume.tex` (translated) and `html/index.html` (same content, HTML markup).

**Key differences between versions:**
- `pt-br/resume.tex` uses `\usepackage[brazil]{babel}` and full name "Vinicius Cubas Brand" (vs "Vinicius Brand" in English)
- HTML uses Inter font via Google Fonts; print styles hide the footer and remove box shadows
- Technical terms in the Portuguese version remain in English (standard in Brazilian tech)

## LaTeX Template

Uses Jake's Resume template (single-column, ATS-compatible). Custom commands:
- `\resumeSubheading{org}{date}{title}{location}` — job/education entry header
- `\resumeDescription{text}` — italic context line beneath a subheading (no bullet)
- `\resumeItem{text}` — bullet point inside `\resumeItemListStart`/`\resumeItemListEnd`
- `\resumeSubHeadingListStart`/`\resumeSubHeadingListEnd` — wraps all entries in a section
