# AI Humanizer Skill

## What This Is

A Claude Code skill that rewrites AI-generated text to pass all major AI detectors (GPTZero, Turnitin, Originality.ai, Grammarly AI Detector) while reading as authentically human writing. Designed to be publicly distributed and installed by anyone via git clone. The skill lives in three files: SKILL.md (the 8-step process), references/kill-list.md (vocabulary and pattern reference), and references/examples.md (before/after rewrites across formats).

## Core Value

The humanization must be so accurate and thorough that text passes every major detector AND convinces human readers — one without the other is a failure.

## Requirements

### Validated

- ✓ 8-step humanization pipeline (context → vocab → structure → rhythm → authenticity → punctuation → dual-pass calibration → delivery check) — existing
- ✓ 7-tier kill list with model-specific flags and replacements — existing
- ✓ Dual-pass calibration system (Detector Pass + Reader Pass) — existing
- ✓ Authenticity scoring across 5 dimensions — existing
- ✓ Register guide across 7 formats — existing
- ✓ Model fingerprint awareness (ChatGPT / Claude / Gemini / GPT-5+) — existing
- ✓ Before/after examples across 6 formats — existing
- ✓ Public GitHub repo at github.com/Gal3xy/ai-humanizer-skill — existing

### Active

- [ ] Kill list expanded with edge cases and false-positive guards
- [ ] Multi-pass strength levels (Light / Standard / Aggressive) based on input AI score
- [ ] Register mismatch detection — flag inconsistent voice before rewriting
- [ ] Academic citation preservation mode — leave citations/quotes untouched
- [ ] Skill description optimized for reliable triggering in Claude Code
- [ ] README accurately reflects full capability and install process
- [ ] Skill validated against real detector tools on real text samples

### Out of Scope

- Web app or UI — this is a Claude Code skill, not a standalone product
- API or programmatic access — out of scope for v1
- Paid tiers or access control — public and free
- Automated detector score simulation — would require third-party API integrations

## Context

Built in a single session. The skill already exists and is functional. The codebase is the skill itself — three markdown files in a specific structure. All improvements are content changes to those files, not code changes. The primary risk is over-engineering: adding complexity that makes the skill slower to use without improving rewrite quality.

The user's explicit preference: minimal surface area, maximum humanization quality. Every addition should directly improve the accuracy or efficiency of the rewrite — nothing decorative.

## Constraints

- **Format**: Claude Code skill — SKILL.md + references/ only, no scripts or executables
- **Length**: SKILL.md should stay under 500 lines to load fully into context on every invocation
- **Scope**: Content-only changes — no new file types, no dependencies
- **Distribution**: Must install cleanly via `git clone` into `~/.claude/skills/`

## Key Decisions

| Decision | Rationale | Outcome |
|---|---|---|
| Keep examples.md | Examples demonstrate both calibration passes and teach the process; cutting them saves nothing | — Pending |
| Keep authenticity scoring | 5-dimension score gives Claude a concrete threshold to hit; without it the check is vague | — Pending |
| Keep model fingerprints | Knowing the source model sharpens cleanup; adds ~20 lines, high value | — Pending |
| Minimal = efficient, not sparse | User confirmed: minimal means the process runs clean, not that content gets cut | ✓ Good |

---
*Last updated: 2026-03-19 after initialization*
