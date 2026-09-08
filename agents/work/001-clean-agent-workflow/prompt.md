# Task Prompt

- Ticket: `001-clean-agent-workflow`
- Status: Done
- Aim: Enforce a question-first, explicitly approved AI workflow and provide concise private note templates for solution and review papers.
- Scope:
  - `AGENTS.md`
  - `agents/rules.md`
  - `agents/config.md`
  - `agents/prompt.md` (move only)
  - `agents/completion.md` (move only)
  - Opening template block in `review_paper/references.bib`
  - This ticket's `prompt.md` and `completion.md`
- Changes:
  - Require the agent to inspect relevant files and ask focused questions before creating a work directory or `prompt.md`.
  - Require all questions about the aim, scope, inputs, decisions, exclusions, acceptance criteria, and verification to be resolved without silent assumptions.
  - After the questions are resolved, require the agent to create a `Ready` prompt from the answers and return it to the user.
  - Require the user to paste the ticket's execution prompt before substantive work begins; only then may its status change to `Approved` or `In progress`.
  - Require a Git status check before work starts. If pre-existing uncommitted changes exist, stop and ask how to handle them; never discard them silently.
  - Move `agents/prompt.md` and `agents/completion.md` into `agents/templates/`, updating every repository reference to those templates.
  - Replace the invalid opening block in `review_paper/references.bib` with two commented, copyable `annote` templates:
    - Solution/empirical paper: problem or gap, approach, evidence/results, limitation, and use in the literature review.
    - Review/survey paper: scope, review method/coverage, main synthesis, research gaps, and use in the literature review.
  - Label the templates as private writer notes. Use `annote` so copied notes remain separate from the published abstract and are not rendered by the current IEEE bibliography style.
- Acceptance criteria:
  - The documented workflow does not create a ticket until all necessary questions have been answered.
  - Substantive work cannot begin until the user pastes the execution prompt.
  - The documented workflow checks for pre-existing uncommitted changes before work begins.
  - Both template files exist under `agents/templates/`; their former paths no longer exist; all references use the new paths.
  - The bibliography begins with exactly two concise, fully commented reading-note templates using `annote`.
  - The note headings are useful for later literature-review synthesis and contain no unnecessary sections.
  - Existing bibliography entries and research notes remain unchanged.
- Out of scope:
  - Fixing structural errors, metadata, spelling, or formatting in existing bibliography entries and notes; that will be a separately discussed ticket.
  - Editing the starter journal paper, its references, or its figures.
  - Committing or pushing changes to `master`.
- Open questions: None.
- Verification:
  - Run `git diff --check`.
  - Review `git status --short` and `git diff --stat`.
  - Search the repository for stale `agents/prompt.md` and `agents/completion.md` template references.
  - Confirm every line of the opening bibliography templates is commented.
  - Confirm the first existing BibTeX entry and everything after it are unchanged.

## Execution Prompt

Execute ticket `001-clean-agent-workflow` exactly as written in `agents/work/001-clean-agent-workflow/prompt.md`. Follow `AGENTS.md`, `agents/rules.md`, and `agents/config.md`. Make only the approved changes, verify every acceptance criterion, set the ticket status to `Done`, and create `completion.md` from `agents/templates/completion.md`.
