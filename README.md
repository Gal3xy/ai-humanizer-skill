# AI Humanizer Skill

A Claude Code skill that rewrites AI-generated text to sound authentically human — bypassing AI detectors (GPTZero, Turnitin, Originality.ai, Grammarly AI Detector) and resonating naturally with human readers.

## What it does

Takes AI-generated text and rewrites it by:
- Stripping flagged vocabulary (the "kill list" — 7 tiers of patterns)
- Removing structural AI fingerprints: copula avoidance, synonym cycling, rule-of-three forcing, inline-header bullets
- Fixing sentence rhythm for natural burstiness variation
- Injecting human markers: opinions, concrete specifics, rhetorical questions, informal register dips
- Running a self-audit pass — after the draft, asks "what still sounds AI?" and revises again
- Matching tone to context (academic, LinkedIn, blog, email, etc.)
- Passing a 14-point final quality check before output

## Installation

```bash
git clone https://github.com/Gal3xy/ai-humanizer-skill.git ~/.claude/skills/ai-humanizer
```

## Usage

The skill triggers automatically in Claude Code when you:
- Paste AI-generated text and ask to humanize it
- Say things like "make this not sound like AI"
- Ask to pass Turnitin, GPTZero, or any AI detector
- Request that writing sound more natural or human

## Structure

```
ai-humanizer-skill/
├── SKILL.md                  # Core skill instructions (7-step process)
└── references/
    ├── kill-list.md          # Full categorized AI word/phrase kill list
    └── examples.md           # Before/after rewrites across contexts
```

## How it works

The skill is built around two core signals that AI detectors use:

1. **Perplexity** — AI text is too predictable. The skill introduces lexical surprise.
2. **Burstiness** — AI sentences are uniform in length. The skill applies a rhythm formula to create natural variation.

Beyond detection, it targets vocabulary, structural patterns, punctuation fingerprints, and tone homogeneity — the things that make humans think "that sounds like ChatGPT" even before any detector runs.

## Register guide

The skill adapts output to context:

| Format | Contractions | Formality | Personal Voice |
|---|---|---|---|
| Academic essay | Low | High | Very low |
| LinkedIn post | Medium | Medium | High |
| Blog post | High | Low–medium | High |
| Business email | Medium | Medium–high | Low |
| News article | Low | High | None |
| Creative writing | Very high | Low | Very high |

## License

MIT
