# PromptKit 🧰

A version-controlled home for my AI **system prompts**, **domain extensions**, working prompts, and the docs that keep everything clear and reusable.

---

## Folder Structure 📁

| Layer | Role | File path |
|-------|------|-----------|
| **Universal Core Foundation** | Baseline “operating system” that defines objectives, thinking principles, behavioural rules, comms rules, system rules, and response architecture. | [`templates/universal-core-foundation-v1.1.md`](templates/universal-core-foundation-v1.1.md) |
| **Domain Extensions** | Add-on templates that *supplement or override* the baseline for a specific role (e.g. Creative Strategist, Future Trend Forecaster, Synthetic Strategist). | [`templates/extensions/`](templates/extensions/) |
| **Working Prompts** | Project-specific or task-specific prompts that import the Core + relevant Extension and add any situational tweaks. | [`prompts/`](prompts/) |

## PromptKit Framework 🏗️

| Level | Purpose | Precedence | Typical file |
|-------|---------|------------|--------------|
| 1. **Universal Core Foundation** | Shared “OS” for every prompt: objectives, thinking principles, behaviour, communication rules, system commands, response architecture. | **Lowest** – everything else can extend / override it. | [ |
| 2. **Domain Extensions** | Opt-in overlays that add or override rules for a specific role or context (Creative Strategist, Trend Forecaster, Synthetic Strategist, etc.). | Middle – can’t change Universal *META-RULES* but can tweak objectives, tone, or add new sections. | Files inside [`templates/extensions/`](templates/extensions/) |
| 3. **Working Prompt** | Final, runnable prompt for a project or task. It imports the Core + chosen Extension(s) and adds situational instructions, examples, or datasets. | **Highest** – last mile tweaks win if they don’t conflict with higher-level META-RULES. | Your file in [`prompts/`](prompts/) |

**Inheritance & override rules** 🧩
1. **Start** with the Universal Core Foundation – always included.  
2. **Layer** one (or more) Domain Extensions when the task fits that persona or lens.  
3. **Compose** the Working Prompt:  
   - Copy a scaffold from `templates/`,  
   - Cite the Extension(s) you’re using in front-matter or comments,  
   - Add project-specific content.  
4. **Precedence:**  
   - Working Prompt content > Extension additions/overrides > Core rules.  
   - *META-RULES* in the Core (e.g. “never fabricate sources”) can **never** be nullified.

**Why this design?**

- **Single Source of Truth** – update the Core once; all descendants inherit.  
- **Composable Overlays** – mix-and-match Extensions without duplicating boilerplate.  
- **Explicit Overrides** – every deviation is documented in its Extension, keeping audits clean. 
---

## 📁 Directory overview

| Folder | Use it for … |
| ------ | ------------ |
| **[`prompts/`](prompts/)** | The actual prompts you run & iterate on (one prompt per file). |
| **[`templates/`](templates/)** | Blueprints to copy when making new prompts. |
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
