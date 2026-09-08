# Completion

- Status: Done
- Summary: Added the question-first approval workflow, relocated the agent templates, and added two concise private reading-note templates.
- Changes:
  - Updated `AGENTS.md` and `agents/rules.md` to require resolved questions, a clean-state check, a `Ready` prompt, and pasted execution approval before substantive work.
  - Updated `agents/config.md` and moved the prompt and completion templates into `agents/templates/`.
  - Replaced only the opening block of `review_paper/references.bib` with commented `annote` templates for solution/empirical and review/survey papers.
- Verification:
  - `git diff --check` passed.
  - Confirmed the former template paths are absent and both new template paths exist.
  - Confirmed all opening template lines are comments.
  - Confirmed all existing bibliography content from `schuldt2004` onward is byte-for-byte unchanged (SHA-256 `a52aa81ce7223218228b13fb984027296be8c324b223e4ff62c88e450823e613`).
  - Confirmed the installed `IEEEtran.bst` does not render the `annote` field.
- Remaining issues: Pre-existing errors and note cleanup elsewhere in `review_paper/references.bib` remain for a separately discussed ticket.
