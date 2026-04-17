# 🗺️ ROADMAP — claude-sessions (real-world example)

> Future plans for the claude-sessions ecosystem (`/archive` + `/time-machine` + scripts).
> Tiered by **"actually helping the user right now"** — not by "what's technically cool."

---

## 📊 Current state (as of 2026-04-17)

- 27 sessions archived
- 1 course in Courserafied (109 entries)
- Single user, local use, grep-based search
- No reported search misses, no noise problems

---

## 🥇 TIER 1 — Build this week (earned)

### T1.1 — Session summary on `/archive now`
**What:** After archiving, auto-extract top 3 insights + top 3 artifacts + what's still dirty.
**Why earned:** Daily recap trains brain to notice high-signal output. Zero cost.
**Trigger:** already earned. Build this week.
**Cost:** ~30 lines of Python.

### T1.2 — Orphan session detection
**What:** Flag sessions with no tags, placeholder summary, no cross-links.
**Why earned:** 25 of 27 sessions are `proposed-untagged`. Info black holes forming NOW.
**Trigger:** already earned. Build this week.
**Cost:** ~20 lines in `regen-index.py`.

### T1.3 — Missed-query log for `/time-machine`
**What:** When a search returns zero results, log the query.
**Why earned:** Best signal of what you're trying to retrieve that isn't captured.
**Trigger:** already earned. Build this week.
**Cost:** ~5 lines in the skill.

---

## 🥈 TIER 2 — Build when usage data warrants (weeks out)

### T2.1 — Retrieval heatmap
**What:** Track which sessions get searched/cited most.
**Trigger:** 50+ /time-machine calls logged.

### T2.2 — Answer freshness flag
**What:** Flag "draws from session N days ago" on search results.
**Trigger:** Archive consistently has sessions > 90 days old.

### T2.3 — Cross-reference surfacing
**What:** When searching X, show co-occurring topics Y, Z.
**Trigger:** 50+ sessions spanning 5+ distinct topic tags.

---

## 🥉 TIER 3 — Helpful at scale (months out)

### T3.1 — Hierarchical tagging conventions
**Trigger:** 20+ tags in flat structure.

### T3.2 — Confidence scoring on search results
**Trigger:** Queries regularly returning 10+ results.

### T3.3 — Decay weighting
**Trigger:** 200+ sessions where age blurs relevance.

---

## 💀 TIER 4 — Overkill for solo use (never unless promoted)

- Semantic embeddings + vector DB
- Agent-specific memory silos
- Reproducible context snapshots
- Multi-user access control
- Distributed retrieval

---

## 🔁 Promotion rules

- Items move UP when trigger fires
- Items move DOWN when built too early or superseded
- Items get KILLED when the problem never materialized

---

## 📜 ROADMAP CHANGELOG

### 2026-04-17 — Initial roadmap
- 4-tier structure established
- 9 items distributed across tiers (3 each in T1, T2, T3; 5 in T4)
- No items shipped yet

---

## 🧬 Principles

1. Earn your features — nothing ships until pain is real
2. Plain text forever
3. Solo-user scale — designed for one person over 20 years
4. Composition over complexity
5. Observable reality — every tier has a concrete trigger
