# Agents

How agents must handle this project.

## Before any work

1. If `START.md` exists, read it fully and follow it **before anything else**. Setup replaces placeholders; when setup finishes in that project, remove this bullet and delete `START.md` (do not remove them from a reusable scaffold/template).
2. Read this file fully.
3. Read all of `CONTEXT/` (ARCHITECTURE, TECHSTACK, IMPORTANT_CHOICES).
4. Prefer existing patterns over inventing new ones.
5. If CONTEXT and code disagree, treat CONTEXT as intent and flag the mismatch; do not silently ignore either.

## Scope rules

- Do not invent production architecture that contradicts `CONTEXT/ARCHITECTURE.md`.
- Do not add languages, frameworks, or major libs without updating `CONTEXT/TECHSTACK.md`.
- Do not reverse a decision in `CONTEXT/IMPORTANT_CHOICES.md` without an explicit human request and a doc update in the same change.
- Prefer small, reviewable diffs. No drive-by refactors.

## Documentation duty

When a change affects design, stack, or a standing decision:

1. Update the matching file under `CONTEXT/`.
2. Keep `README.md` accurate if purpose or status shifts.
3. Leave docs shorter and truer, not longer and vaguer.

## Greenfield state

Repo starts empty of application code. Until code exists:

- Do not pretend features, APIs, or folders exist.
- Propose structure that matches CONTEXT; implement only what the human asked for.
- When first real modules land, update ARCHITECTURE and TECHSTACK in the same change.

## Safety and quality

- No hardcoded secrets or credentials.
- Sanitize untrusted input at trust boundaries.
- Prefer parameterized queries / safe APIs over string concatenation for data access.
- Check return values from critical calls; do not swallow errors in empty catches.
- Make use of .gitignore file
- NEVER do any destructive if not authorized by the user.

## Communication with humans

- Be direct. State uncertainty with “I am not sure” when unsure.
- Do not commit or push unless the human explicitly asks.
- Do not expand scope beyond the request.
