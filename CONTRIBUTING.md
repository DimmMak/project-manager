# 🤝 Contributing to project-manager

PRs welcome. Highest-impact contributions:

---

## 🆕 New subcommand

Think of a PM duty we missed. Document it:
1. Add the subcommand spec to `SKILL.md` under the SUBCOMMANDS section
2. Add a row to the command table in `README.md`
3. Mention the new subcommand in `CHANGELOG.md`
4. Open a PR with a short rationale

Good candidate subcommands we considered but skipped:
- `/project-manager export csv` — emit roadmap as CSV for spreadsheet users
- `/project-manager gantt` — generate a text-based Gantt chart of ships
- `/project-manager conflicts` — detect dependencies between items
- `/project-manager snapshot` — archive the current roadmap state before big changes

---

## 🎭 New PM behavior

If you have a PM practice you'd like enforced by the agent (e.g., a specific review cadence, a stakeholder comms pattern, a specific failure-mode flag), propose it in `SKILL.md` under "PM AGENT BEHAVIORS."

---

## 🧪 New template variants

`templates/ROADMAP.template.md` is the default. Variants for specific domains could live alongside:
- `templates/ROADMAP.saas-product.template.md`
- `templates/ROADMAP.open-source.template.md`
- `templates/ROADMAP.personal-learning.template.md`

Domain-specific triggers and examples help contributors get started faster.

---

## 🐛 Bug reports

Open an issue with:
- Project's ROADMAP.md schema (sanitized)
- Subcommand run
- Expected vs actual behavior
- Snippet of output if available

---

## 📜 Code style

- Markdown with functional emojis paired
- Tables over prose for rules and commands
- Preserve "stakeholder-grade" brevity in example outputs
- No dependencies added — stays as pure markdown + shell-friendly

---

## 🚫 Rejected PR categories

- Adds heavy runtime dependencies (the skill stays pure markdown)
- Removes the tier structure (4-tier is the enforced abstraction)
- Breaks the earn-your-features discipline (e.g., auto-promotes without evidence)
- Turns ROADMAP.md into a DB / JSON / binary format (plain text forever)

---

🗺️📋 Thanks for contributing.
