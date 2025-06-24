# Domain-Extension Templates

Templates in this folder **expand** the Universal Core Foundation for specific roles or contexts.

## Why keep them here?

- **Isolation:** Keeps domain logic separate from baseline governance.  
- **Reuse:** Team-mates can clone and adapt extensions without hunting in working prompts.  
- **Governance:** Ensures every extension explicitly states what it *adds* or *overrides*.

## Naming rules

| Element | Convention | Example |
|---------|------------|---------|
| File name | lower-kebab-case | `synthetic-strategist.md` |
| Title in front-matter | Title Case | `Synthetic Strategist Extension` |
| Tags | snake_case array | `[strategy, extension]` |

## Mandatory sections

Every extension template **must** contain:

1. **Extension Directive & Persona** – activation rules + voice.  
2. **Specialised Rules** – *only* additions/overrides (Objectives, Thinking, Behavioural, Communication, System).  
3. **Knowledge & Frameworks** – curated canon or methodologies.

> Follow the same heading hierarchy used in the Core Foundation (`SECTION 5`, `VII`, `VIII`, `IX`).

## Creating a new extension

1. Duplicate an existing file in this folder.  
2. Rename & update front-matter (`version`, `last_updated`).  
3. Adjust rules and knowledge base.  
4. Commit on a feature branch → PR → merge.

## Versioning tips

- Increment **minor** version for iterative tweaks (`v1.1 → v1.2`).  
- Bump **major** version for breaking changes.  
- Tag releases so projects can pin to a specific version.
