# promptkit

A version-controlled home for my AI **system prompts**, **domain extensions**, working prompts, and the docs that keep everything clear and reusable.

---

## 🧩 Prompt architecture

| Layer | Role | File path |
|-------|------|-----------|
| **Universal Core Foundation** | Baseline “operating system” that defines objectives, thinking principles, behavioural rules, comms rules, system rules, and response architecture. | [`templates/universal-core-foundation-v1.1.md`](templates/system/universal-core-foundation.md) |
| **Domain Extensions** | Add-on templates that *supplement or override* the baseline for a specific role (e.g. Creative Strategist, Future Trend Forecaster, Synthetic Strategist). | [`templates/extensions/`](templates/extensions/) |
| **Working Prompts** | Project-specific or task-specific prompts that import the Core + relevant Extension and add any situational tweaks. | [`prompts/`](prompts/) |

**Working theory**

1. **Single Source of Truth** – The Universal Core Foundation is edited *in-place* and version-tagged. Everything inherits from it, so one change propagates everywhere.  
2. **Composable Overlays** – Extensions are opt-in overlays. They declare **only** what they add or override, keeping inheritance explicit and debuggable.  
3. **Copy-to-Create** – New prompts start by copying a template, then trimming or augmenting. This enforces consistent front-matter and section ordering.  
4. **Version Tags as APIs** – Core and Extension files are tagged (`v1.1`, `v1.2`). Projects can pin to a tag for stability while upstream evolves.  

---

## 📁 Directory overview

| Folder | Use it for … |
| ------ | ------------ |
| **[`prompts/`](prompts/)** | The actual prompts you run & iterate on (one prompt per file). |
| **[`templates/`](templates/)** | Blueprints to copy when making new prompts. |
| **[`templates/system/`](templates/system/)** | Core governance & meta-prompts. |
| **[`templates/extensions/`](templates/extensions/)** | Domain add-ons that *supplement / override* the baseline. |
| **[`docs/`](docs/)** | Project docs, style rules, decision records, changelogs. |
| **`.gitignore`** | Ignore list for OS cruft, IDE files, logs, etc. |
| **`README.md`** | This file. |

---

## 🛠️ Workflow conventions

| Guideline | Why |
| ---------- | --- |
| **Branches:** `feat/`, `fix/`, `docs/`, `chore/` | Keeps commit history readable via Conventional Commits. |
| **PRs for everything** | Guarantees review—even when working solo. |
| **Tags = versions** | Tag every merge that changes a system or extension template. |
| **Single-source-of-truth** | Iterate in-place; copy files only for breaking rewrites (`v2.x`). |
| **One prompt ≠ many prompts** | Each prompt lives in its own file for granular diffs. |

---
