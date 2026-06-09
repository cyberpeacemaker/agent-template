# General Guidance

### 🚀 Core Workflow

* **Execution Cycle:** Follow a strict, sequential loop: **Plan** $\rightarrow$ **Deconstruct** (into sub-tasks) $\rightarrow$ **Implement** (one step at a time) $\rightarrow$ **Verify** (confirm current outcome passes before moving forward).
* **Validation:** Test all hypotheses explicitly. Use the utilities in `scripts/` or write new verification scripts to check results. **Do not guess or assume success.**
* **Planning Template:** For multi-step tasks, you must print a brief plan using this exact structure before writing code:
```markdown
  1. [Sub-task] → verify via: [explicit check/test]
  2. [Sub-task] → verify via: [explicit check/test]
```

### 🧠 Anti-Assumption Rules

* **Stop on Ambiguity:** If a request has multiple interpretations, present them clearly—do not pick one silently. If something is unclear, stop and explicitly ask. You are encouraged to ask as many questions as needed.
* **Surface Tradeoffs:** State assumptions explicitly before implementing. If a simpler or safer architectural approach exists, propose it and push back if warranted.
* **Verifiable Goals:** Transform all tasks into distinct goals with clear success criteria. Loop execution until criteria are met.

### 📝 Repository Maintenance

* **Documentation:** Immediately update relevant `README` files following any code or structural changes.
* **Link Integrity:** If file paths change, instantly audit and fix all internal cross-references and markdown links.

---

# Project Constraints

* **Scope Isolation:** Strictly ignore all files under `docs/` and the `TODO.md` file.
<!-- * **Module Architecture:**
* Code under `@modules/delta/` currently contains only quiz structures.
* When expanding this directory, transform it into a functional module/playbook by appending solutions, strictly adhering to the design patterns found in `@module_create_template.md` and `@module_create_rule.md`.
* **Tooling:** Utilize the `.claude/create-module` skill for all module generation tasks. -->

