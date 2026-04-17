# 🗺️📋 project-manager

> **A Product Manager in a `.skill` file.** Plays the corporate role of a PM for any repo with a ROADMAP.md — triage, prioritization, sprint planning, shipping rituals, retrospectives, stale-item flagging — so the human building things doesn't have to.

```
YOU                           /project-manager                 RESULT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
"what's the plan?"            /project-manager status          Executive snapshot
"what should I build?"        /project-manager review          Trigger audit + recs
"ship T1.1"                   /project-manager ship            CHANGELOG updated
"promote T2.1"                /project-manager promote         Evidence-gated
"kill T3.2"                   /project-manager kill            Rationale documented
"weekly plan"                 /project-manager plan            Sprint laid out
"retro the month"             /project-manager retro           What shipped / missed
```

**You never touch ROADMAP.md manually.** The agent keeps it honest.

---

## 🎯 Why this exists

Solo builders don't usually have Product Managers. So they ship features impulsively, forget to kill dead plans, let roadmaps go stale, and build speculative complexity that never earns its place.

`/project-manager` installs the **PM discipline** as a skill:
- No item enters "priority" without evidence
- No item stalls silently in high-priority tier
- No kills happen without documentation
- Every ship gets a retrospective

It's the earn-your-features principle, enforced by an agent.

---

## 🚀 Quick start

### Install

```bash
# Clone the repo
git clone https://github.com/DimmMak/project-manager.git
cd project-manager

# Install as a .skill (both dir + zip for compatibility)
mkdir -p ~/.claude/skills/project-manager
cp SKILL.md ~/.claude/skills/project-manager/
zip -r ~/.claude/skills/project-manager.skill project-manager/ 
```

### Initialize a roadmap

In any repo:

```
/project-manager init
```

Creates a fresh `ROADMAP.md` in the current directory from the template.

### Use it

```bash
/project-manager status                  # executive summary
/project-manager add 2 "Add dark mode" "users keep asking"
/project-manager review                  # weekly triage ritual  
/project-manager ship T1.1 "shipped as planned in PR #42"
/project-manager plan                    # what to ship this week
/project-manager retro                   # monthly retrospective
```

---

## 📋 The 11 subcommands

| Command | What it does |
|---|---|
| `/project-manager status` | Executive snapshot (tier counts, last update, blockers) |
| `/project-manager review` | Weekly triage + trigger audit + recommendations |
| `/project-manager ship {ID} "notes"` | Mark item shipped, move to CHANGELOG |
| `/project-manager promote {ID} {tier} "why"` | Move item up a tier |
| `/project-manager demote {ID} {tier} "why"` | Move item down a tier |
| `/project-manager kill {ID} "why"` | Remove from plan, document rationale |
| `/project-manager add {tier} "title" "why"` | Add new item to specified tier |
| `/project-manager audit` | Flag stalled items |
| `/project-manager plan` | Weekly sprint plan |
| `/project-manager retro` | Monthly retrospective |
| `/project-manager show {tier}` | Filter view to one tier |
| `/project-manager init` | Create ROADMAP.md from template |

---

## 🎭 PM behaviors baked in

The agent enforces discipline you'd want from a real PM:

**Triage-first.** Won't let items enter T1 by default. Requires evidence.
**Kill-friendly.** Celebrates kills in retros. Killing speculative features is a WIN.
**Evidence-driven.** Promotions require verifiable signal, not gut feel.
**Honest retros.** If shipped features went unused, says so.
**Stakeholder reports.** 10-second snapshots, not essays.

---

## 🏗️ The 4-tier system

```
🥇 TIER 1 — build this week (earned by real pain)
🥈 TIER 2 — waiting on triggers (weeks out)
🥉 TIER 3 — helpful at scale (months out)
💀 TIER 4 — overkill for current scale (never build unless promoted)
```

Items move BETWEEN tiers as evidence accumulates. Movement is always documented in the CHANGELOG section.

---

## 📂 Repo layout

```
project-manager/
├── README.md                      # This file
├── SKILL.md                       # The Claude skill spec
├── CHANGELOG.md                   # Version history
├── CONTRIBUTING.md                # Contribution guide
├── LICENSE                        # MIT
├── .gitignore
├── templates/
│   └── ROADMAP.template.md        # Scaffold for new projects
└── examples/
    └── example-roadmap.md         # Sample filled-in roadmap
```

---

## 🧬 Design principles

1. **Earn your features** — nothing ships without evidence of real pain
2. **Repo-agnostic** — works on any project with a ROADMAP.md
3. **Plain text forever** — ROADMAP.md is the single source of truth
4. **Composition-friendly** — pairs with other agents (mewtwo, etc.)
5. **Stakeholder-grade reporting** — outputs readable in seconds, not essays

---

## 🔗 Pairs with

Works alongside any agent ecosystem. Especially useful with:

- **mewtwo** — orchestrate `review` across all your project roadmaps at once
- **claude-sessions** — keeps the archive ecosystem's roadmap healthy
- **cash-out** — weekly review can be part of your end-of-week ritual

---

## 📜 License

MIT — use it wherever.

---

## 🎯 Status

**v1.0.0 — Shipping.** PM agent spec stable. Tested against claude-sessions roadmap.

🗺️📋🃏
