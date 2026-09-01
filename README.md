# PhD Work

PhD research papers on video processing and unusual human-activity classification
from surveillance video. Each paper is stored in its own directory and written in
LaTeX with BibTeX references.

## Build a paper

From PowerShell, run the following commands to build the starter journal paper and
resolve its citations and cross-references:

```powershell
cd starter_journal
pdflatex -interaction=nonstopmode -file-line-error starter_journal.tex
bibtex starter_journal
pdflatex -interaction=nonstopmode -file-line-error starter_journal.tex
pdflatex -interaction=nonstopmode -file-line-error starter_journal.tex
```

The generated file is `starter_journal/starter_journal.pdf`.
