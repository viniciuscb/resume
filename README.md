# Vinicius Brand — Resume

Resume in three parallel formats, kept in sync.

## Formats

| Format | File | Output |
|---|---|---|
| LaTeX (English) | `resume.tex` | `resume.pdf` |
| LaTeX (Portuguese) | `pt-br/resume.tex` | `pt-br/resume.pdf` |
| HTML/CSS | `html/index.html` | Print to PDF via browser |

## Building

**PDF from LaTeX:**
```bash
pdflatex resume.tex          # English
cd pt-br && pdflatex resume.tex   # Portuguese
```

**HTML version:** Open `html/index.html` in a browser. Print with Ctrl+P → Save as PDF.

## Structure

- English `.tex` is the canonical source of truth
- Changes propagate to `pt-br/resume.tex` (translated) and `html/index.html`
- Technical terms in the Portuguese version remain in English
