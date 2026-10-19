# Project setup

Agent: read this file fully before any other work. Follow it to turn this scaffold into a real project. Do not invent features beyond what the human describes.

## Goal

Fill the placeholder docs so they describe **this** project. Leave the folder layout as-is unless the human asks otherwise.

Required files after setup:

| Path | Must contain |
|------|----------------|
| `README.md` | Real project description: purpose, how to run (if known), docs map |
| `AGENTS.md` | Agent rules for ongoing work (already present; trim setup-only bits at end) |
| `CONTEXT/ARCHITECTURE.md` | How the system is structured and where boundaries sit |
| `CONTEXT/TECHSTACK.md` | Languages, tools, major dependencies |
| `CONTEXT/IMPORTANT_CHOICES.md` | Hard-to-reverse decisions agents must not silently undo |

## Setup steps

1. **Gather intent from the human**
   - What problem does the project solve?
   - Who is it for?
   - Language / runtime preferences?
   - Non-goals?
   - Ask if anything critical is missing. Do not guess stack or architecture when the human has not said.

2. **Write `README.md`**
   - Replace the placeholder with a clear description.
   - Include a short docs map pointing at `AGENTS.md` and `CONTEXT/`.
   - Status: honest (prototype, MVP, greenfield with first modules, etc.).

3. **Write `CONTEXT/ARCHITECTURE.md`**
   - Layers, main components, trust boundaries, side-effect paths.
   - Expected repo layout once code exists.
   - Non-goals if useful.
   - No fake modules: only what the human committed to or clearly asked for.

4. **Write `CONTEXT/TECHSTACK.md`**
   - Primary language, package manager, key libs, test/CI approach.
   - Mark anything still open as TBD.
   - Rules for changing the stack (update this file in the same change).

5. **Write `CONTEXT/IMPORTANT_CHOICES.md`**
   - Standing decisions (short headings + 1–2 sentences each).
   - Open decisions list if needed.
   - How to add a new choice.

6. **Align `AGENTS.md` for ongoing work**
   - Keep safety, scope, docs-duty, and communication rules.
   - Ensure “Before any work” tells agents to read `AGENTS.md` then all of `CONTEXT/` (not this file).
   - Remove greenfield-only noise only if it no longer applies.

7. **Finish setup (cleanup — only in the project you just set up)**
   - Delete this file (`START.md`).
   - In `AGENTS.md`, remove any instruction to read `START.md` before other work.
   - Do **not** treat the scaffold/template repo as the place to delete these; cleanup belongs in the project whose placeholders you just filled.

## Done when

- Placeholders in `README.md` and all `CONTEXT/*` files are gone and replaced with project-specific content.
- `AGENTS.md` no longer mentions `START.md`.
- `START.md` is deleted in that project.
- Human has confirmed the written purpose, architecture, stack, and choices (or explicitly deferred open items as TBD in CONTEXT).

## Do not

- Commit or push unless the human asks.
- Remove `START.md` or the “read START.md first” rule from a template/scaffold copy that is meant to stay reusable.
- Invent production architecture or a stack the human did not choose.
