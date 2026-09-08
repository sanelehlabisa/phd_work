# AI Working Guide

## Repository

- This repository contains PhD papers on video processing and classification of unusual human activities in surveillance video.
- Each paper lives in its own directory.
- Papers use LaTeX, BibTeX references, and figures. This is not an application-code repository.
- Keep LaTeX readable and consistently formatted.
- Use the repository CLI commands to build PDFs and resolve references.

## Workflow

1. Read the relevant paper files and the guidance in `agents/`, then check
   `git status` before setting up the task.
2. If there are pre-existing uncommitted changes, stop and ask the user how to
   handle them. Never discard or overwrite them silently.
3. Discuss substantial work with the user and ask short, focused questions until
   the aim, scope, inputs, decisions, exclusions, acceptance criteria, and
   verification are explicit. Do not silently assume missing requirements.
4. Do not create a work directory or `prompt.md` while any required question is
   unanswered.
5. Once all questions are answered, create the next
   `agents/work/NNN-short-title/` directory and use
   `agents/templates/prompt.md` to record the answers in a `Ready` prompt.
6. Return the completed prompt and its execution prompt to the user.
7. Do not begin substantial edits until the user pastes the execution prompt.
   After that approval, set the prompt status to `Approved`, then `In progress`.
8. Make only the approved changes and verify every acceptance criterion.
9. Set the prompt status to `Done` and create `completion.md` from
   `agents/templates/completion.md`.

Small typo fixes or explanations do not require a ticket unless the user asks for one.

## Rules

- Do not invent research results, citations, datasets, or claims.
- Preserve the author's meaning and academic voice.
- Ask before changing the paper structure, research claims, or bibliography.
- Ask rather than guess when a missing decision could affect the work.
- Keep generated LaTeX files out of source changes unless explicitly requested.
- Never delete user content without explicit approval.
- Follow `agents/rules.md` and `agents/config.md`.
