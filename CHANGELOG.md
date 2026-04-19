# 📜 project-manager Changelog

## v0.2.0 — 2026-04-18

**World-Class Overhaul shipped.** Part of the fleet-wide upgrade to tree+plugin+unix architecture.

- 🌳 **Tree:** `domain:` field added to frontmatter (general)
- 🎮 **Plugin:** `capabilities:` block declares reads / writes / calls / cannot
- 🐧 **Unix:** `unix_contract:` block declares data_format / schema_version / stdin_support / stdout_format / composable_with
- 🛡️ Schema v0.3 validation required at install (via `future-proof/scripts/validate-skill.py`)
- 🔗 Install converted to symlink pattern (kills drift between Desktop source and live install)
- 🏷️ Tagged at `v-2026-04-18-world-class` for rollback

See `memory/project_world_class_architecture.md` for the full model.

---


## v1.0.0 — 2026-04-17 — Initial Release

### 🚀 Shipped
- **SKILL.md** — full PM agent spec with 11 subcommands
- **Templates** — `ROADMAP.template.md` scaffold for any new project
- **README** — pitch, install, subcommand reference, design principles
- **MIT LICENSE**
- **CONTRIBUTING.md**

### 📋 11 subcommands (full PM coverage)
- `status` — executive snapshot
- `review` — weekly triage + trigger audit
- `ship` — mark item shipped, update CHANGELOG
- `promote` — evidence-gated tier upgrade
- `demote` — document tier downgrade
- `kill` — remove from plan with rationale
- `add` — propose new item in specified tier
- `audit` — flag stalled items
- `plan` — weekly sprint plan
- `retro` — monthly retrospective
- `show` — filter view to one tier
- `init` — scaffold a new ROADMAP.md

### 🎭 PM behaviors enforced
- Triage-first mindset (no items enter T1 by default)
- Evidence-driven promotions (no gut-feel upgrades)
- Kill-friendly culture (kills celebrated in retros)
- Honest retros (unused ships named honestly)
- Stakeholder-grade reporting (snapshots, not essays)

### 💡 Why this exists
Solo builders don't have PMs. So they ship impulsively, forget to kill dead plans, let roadmaps rot, and build speculative complexity. `/project-manager` enforces the **earn-your-features** discipline as an agent so the human building things doesn't have to be their own PM on top of everything else.

### 🏗️ Spawned from
Extracted from the `claude-sessions/skills/roadmap/` skill that originally managed the archive ecosystem's roadmap. Generalized to work with any repo's ROADMAP.md.

### 🔗 Pairs with
- `mewtwo` — orchestrate multi-project roadmap reviews
- `claude-sessions` — archive ecosystem's own roadmap
- Any repo with a ROADMAP.md

🗺️📋🃏
