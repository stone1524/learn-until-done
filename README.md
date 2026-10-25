# learn-until-done

**A learning-coach skill for your coding agent.** It turns "I want to learn X" into a criteria-first, abandonment-proof learning run — and doesn't let either of you declare victory until every demo-able outcome actually passes.

learn-until-done is a systematic-learning methodology distilled from real, completed learning projects (a 10-week technical reading roadmap, a week-by-week study schedule, a tool-tutorial teardown), packaged as a single composable skill. No framework, no dependencies — one folder your agent loads.

## Why

Most learning plans die the same way:

- **No definition of done.** "Finish the course" is not a criterion. You watch, you nod, nothing demo-able remains.
- **Resource hoarding.** Twenty tabs, three courses, no main textbook — so nothing gets read.
- **Week-3 collapse.** The first slip cascades: the plan has no cut rules, so a missed week quietly becomes a missed month.
- **Silent quitting.** Motivation decays without feedback, and nobody notices until the plan is three weeks dead.

learn-until-done encodes the countermeasures as hard gates the agent enforces — not suggestions.

## How it works

Five stages, with gates between them. Nothing advances silently.

1. **Clarify (Stage 0)** — the agent extracts four things before anything else: motivation, **criteria for "learned"** (a demo-able outcomes list + quantitative metrics, written *before* any resource is opened), time budget, hard deadline. No criteria, no start.
2. **Scout & plan (Stage 1)** — one recon pass: pick a **single main resource**, run the official minimal demo first to prove the environment works, then write a single-entry `PLAN.md` — weekly blocks, timeboxes, minimum outcomes ("can open / can run / can demo"), review columns, and the **cut rules for when a week slips, written before work starts**.
3. **Coach the loop (Stage 2)** — weekly: one main line, timeboxed, every outcome verified with evidence (command output / screenshot / recording). Slips trigger the pre-written cut list, never overtime. Only nice-to-haves get cut; **milestones slip, never cancel**.
4. **Accept (Stage 3)** — every criterion from Stage 0, demonstrated live. Not-passed items are explicitly marked "deferred to complete" or "descoped" — never quietly dropped.
5. **Bank it (Stage 4)** — everything lands in `learning/<domain>/`: the plan, notes, artifacts, and a one-line retrospective.

## The rules

- **Criteria before content.** "Finished watching" is not a standard.
- **One main resource.** Good stuff found along the way goes to a "later" list, not the schedule.
- **Cut rules are written before you slip.** A plan without them doesn't pass review.
- **Milestones slip, never cancel.** Deferred-to-complete is allowed; vanished is not.
- **Two silent weeks trigger a protocol, not a lecture.** Split the milestone in half, bring in external feedback — no doubling down on self-discipline.
- **A 3-day sprint never silently becomes a 3-month odyssey.** Changing tier requires an explicit decision.

Three tiers, same spine: **A** month-scale roadmaps · **B** week-scale (1–4 weeks) · **C** day-scale sprints. Smaller tiers shed process weight, never criteria or acceptance.

## What's inside

```text
learn-until-done/
├── SKILL.md                    # the router: tiers, five stages, gates, red flags
└── references/
    ├── tiers.md                # per-tier tailoring matrix
    ├── plan-format.md          # PLAN.md single-entry template (+ C-tier half-pager)
    ├── coaching-rules.md       # weekly review loop, escape hatches, momentum protocol
    └── sources.md              # methodology provenance & maintenance rules
```

## Install

Requires an agent that loads Agent Skills (`SKILL.md` folders) — Claude Code, ZCode, Codex, Cursor and compatible harnesses.

```bash
git clone https://github.com/stone1524/learn-until-done.git
# Claude Code
cp -r learn-until-done/learn-until-done ~/.claude/skills/
# other agents: copy into your skills directory, e.g. ~/.agents/skills/
```

No slash command needed. The skill auto-triggers on phrases like "I want to learn X" / 「我要学 X」, "help me plan learning X", "X 速成" — and stays out of the way for single-concept questions, codebase reading, and dev tasks (explicit NOT-for boundaries in its description).

> **Language note:** the skill's working content (templates, coaching lines) is Chinese (zh-CN); it converses in whatever language you use. English content is on the roadmap. 简体中文说明见 [README.zh-CN.md](./README.zh-CN.md)。

## License

MIT — see [LICENSE](./LICENSE).
