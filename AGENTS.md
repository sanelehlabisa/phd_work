# AI Working Guide

## Repository

- This repository contains PhD papers on video processing and classification of unusual human activities in surveillance video.
- Each paper lives in its own directory.
- Papers use LaTeX, BibTeX references, and figures. This is not an application-code repository.
- Keep LaTeX readable and consistently formatted.
- Use the repository CLI commands to build PDFs and resolve references.

## Workflow

1. Read the relevant paper files and the guidance in `agents/`.
2. If a request is ambiguous, ask short, specific questions before editing.
3. Create the next `agents/work/NNN-short-title/` directory for substantial work.
4. Use `agents/prompt.md` to create the ticket's `prompt.md`.
5. Ask the user focused questions until the ticket is clear.
6. Return the completed prompt to the user for approval before execution.
7. After approval, make only the agreed changes and verify them.
8. Set the prompt status to `Done` and create `completion.md` from `agents/completion.md`.

Small typo fixes or explanations do not require a ticket unless the user asks for one.

## Rules

- Do not invent research results, citations, datasets, or claims.
- Preserve the author's meaning and academic voice.
- Ask before changing the paper structure, research claims, or bibliography.
- Keep generated LaTeX files out of source changes unless explicitly requested.
- Never delete user content without explicit approval.
- Follow `agents/rules.md` and `agents/config.md`.
