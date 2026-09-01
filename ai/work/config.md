# Project Configuration

- Content: PhD research papers on video processing and unusual human-activity classification from surveillance video.
- Structure: One directory per paper.
- Source: LaTeX (`.tex`), BibTeX (`.bib`), and figures.
- Ticket directory: `ai/work/NNN-short-title/`.
- Ticket numbers: Start at `001` and increase sequentially.
- Build: Use a project-provided build command when available; otherwise prefer `latexmk -pdf <main.tex>`.
- References: The final build must resolve citations and bibliography entries.
- Formatting: Use readable indentation, one sentence per source line where practical, and no trailing whitespace.
- Generated files: Do not commit PDF or LaTeX build artifacts unless requested.
