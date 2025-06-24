# Prompt Templates

This folder contains **reusable blueprints** – files you copy-and-tweak when creating new prompts or system directives.  
Nothing here is executed directly; each file is a foundation.

## Structure



| Sub-folder | Purpose |
|------------|---------|
| **`extensions/`** | Domain-specific overlays that supplement / override the baseline. |

## How to use a template

1. **Copy** the file (or click *Use this file* in GitHub UI).  
2. Paste it into `prompts/` (or another working directory).  
3. Update front-matter: `title`, `version`, `last_updated`.  
4. Revise body text → commit with a clear message (e.g., `feat: add brand strategist prompt`).

> **Tip:** Keep *one prompt per file* and use **kebab-case** filenames for readability.

## Versioning

- Minor edits: branch → PR → merge → tag (`v1.2`).  
- Major rewrites: duplicate into a new file (e.g., `universal-core-foundation-v2.0.md`).  
- Always update the `version` field *inside* the file.

## Commit conventions

- `feat(template): …` – new template  
- `fix(template): …` – bug/typo  
- `docs(template): …` – README or comment updates 
