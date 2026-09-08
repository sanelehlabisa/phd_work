# Task Prompt

- Ticket: `002-review-paper-template`
- Status: Done
- Aim: Create a concise LaTeX scaffold that guides the writing of a structured review on abnormal human activity recognition in video surveillance.
- Scope:
  - New file `review_paper/review_paper.tex`.
  - This ticket's `prompt.md` and `completion.md`.
- Changes:
  - Base the document setup and visual conventions on `starter_journal/starter_journal.tex`, while retaining only packages needed by the review scaffold.
  - Use the working title `Abnormal Human Activity Recognition in Video Surveillance: A Review` and reuse the author, university, and email details from the starter journal.
  - Add an abstract and keywords area with short hidden LaTeX comments explaining what to write.
  - Structure the paper with concise sections and subsections for:
    - Introduction: background and motivation, review aim and questions, scope and boundaries, and paper organization.
    - Review Method: search strategy, inclusion and exclusion criteria, study selection, and data extraction and categorization.
    - Abnormal Activity Recognition in Video Surveillance: terminology and task formulations, and surveillance-video challenges.
    - Datasets and Evaluation: benchmark datasets, evaluation metrics, and evaluation protocols.
    - Recognition Approaches: traditional methods, CNN-based methods, 3D CNNs, CNN--RNN and ConvLSTM methods, and transformer-based methods.
    - Comparative Analysis: recognition performance, computational efficiency, and generalization to real surveillance conditions.
    - Research Gaps and Future Directions: dataset limitations, robustness and generalization, computational cost, explainability and localization, and positioning of the PhD research.
    - Conclusion.
  - Put one or two short guidance comments beneath each heading explaining what belongs there; keep these comments hidden from the rendered paper.
  - Include labels and IEEE-style bibliography commands that use the existing `review_paper/references.bib`.
  - Present the document as a structured review with transparent search and selection methods; do not claim it is a completed systematic review or that PRISMA was followed.
- Acceptance criteria:
  - `review_paper/review_paper.tex` exists and follows the agreed structure.
  - The scaffold is simple, concise, and specific to abnormal human activity recognition from surveillance video.
  - Writing guidance is provided only through LaTeX comments and does not appear as paper content.
  - No research findings, citations, datasets, search results, or claims are invented.
  - Existing files in `review_paper/`, including `references.bib`, remain unchanged.
  - The LaTeX scaffold compiles without syntax errors in a temporary output directory; bibliography cleanup and resolution are not part of this ticket.
- Out of scope:
  - Writing the review's academic content or drawing conclusions about the research gap.
  - Adding, removing, correcting, or citing bibliography entries.
  - Performing the literature search, screening papers, or claiming systematic-review compliance.
  - Adding figures, tables, review results, or a PRISMA flow diagram.
  - Editing the starter journal paper.
  - Committing or pushing the completed ticket.
- Open questions: None.
- Verification:
  - Run `git diff --check`.
  - Compile `review_paper.tex` with `pdflatex` in a temporary output directory and confirm there are no LaTeX errors.
  - Check that all instructional text is in `%` comments.
  - Confirm `review_paper/references.bib` and all starter-journal files are unchanged.
  - Review the generated section hierarchy for completeness and concision.

## Execution Prompt

Execute ticket `002-review-paper-template` exactly as written in `agents/work/002-review-paper-template/prompt.md`. Follow `AGENTS.md`, `agents/rules.md`, and `agents/config.md`. Make only the approved changes, verify every acceptance criterion, set the ticket status to `Done`, and create `completion.md` from `agents/templates/completion.md`.
