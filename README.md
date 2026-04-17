# 🗺️📋 future-planner

> **A Product Manager in a `.skill` file.** Plays the corporate role of a PM for any repo with a ROADMAP.md — triage, prioritization, sprint planning, shipping rituals, retrospectives, stale-item flagging — so the human building things doesn't have to.

```
YOU                           /future-planner                 RESULT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
"what's the plan?"            /future-planner status          Executive snapshot
"what should I build?"        /future-planner review          Trigger audit + recs
"ship T1.1"                   /future-planner ship            CHANGELOG updated
"promote T2.1"                /future-planner promote         Evidence-gated
"kill T3.2"                   /future-planner kill            Rationale documented
"weekly plan"                 /future-planner plan            Sprint laid out
"retro the month"             /future-planner retro           What shipped / missed
```

**You never touch ROADMAP.md manually.** The agent keeps it honest.

---

## 🎯 Why this exists

Solo builders don't usually have Product Managers. So they ship features impulsively, forget to kill dead plans, let roadmaps go stale, and build speculative complexity that never earns its place.

`/future-planner` installs the **PM discipline** as a skill:
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
git clone https://github.com/DimmMak/future-planner.git
cd future-planner

# Install as a .skill (both dir + zip for compatibility)
mkdir -p ~/.claude/skills/future-planner
cp SKILL.md ~/.claude/skills/future-planner/
zip -r ~/.claude/skills/future-planner.skill future-planner/ 
```

### Initialize a roadmap

In any repo:

```
/future-planner init
```

Creates a fresh `ROADMAP.md` in the current directory from the template.

### Use it

```bash
/future-planner status                  # executive summary
/future-planner add 2 "Add dark mode" "users keep asking"
/future-planner review                  # weekly triage ritual  
/future-planner ship T1.1 "shipped as planned in PR #42"
/future-planner plan                    # what to ship this week
/future-planner retro                   # monthly retrospective
```

---

## 📋 The 11 subcommands

| Command | What it does |
|---|---|
| `/future-planner status` | Executive snapshot (tier counts, last update, blockers) |
| `/future-planner review` | Weekly triage + trigger audit + recommendations |
| `/future-planner ship {ID} "notes"` | Mark item shipped, move to CHANGELOG |
| `/future-planner promote {ID} {tier} "why"` | Move item up a tier |
| `/future-planner demote {ID} {tier} "why"` | Move item down a tier |
| `/future-planner kill {ID} "why"` | Remove from plan, document rationale |
| `/future-planner add {tier} "title" "why"` | Add new item to specified tier |
| `/future-planner audit` | Flag stalled items |
| `/future-planner plan` | Weekly sprint plan |
| `/future-planner retro` | Monthly retrospective |
| `/future-planner show {tier}` | Filter view to one tier |
| `/future-planner init` | Create ROADMAP.md from template |

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
future-planner/
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
