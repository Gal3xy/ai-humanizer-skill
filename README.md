# AI Humanizer

A Claude Code skill that rewrites AI-generated text to pass detectors and read as authentic human writing.

## What it does

Most humanizers solve one problem and miss the other. Text either passes a scanner but reads as dead, or has personality but still trips technical signals. This skill fixes both.

It works by running text through a two-goal process:

1. **Defeat the detectors** — targets perplexity score, burstiness score, vocabulary fingerprint, and structural fingerprint for GPTZero, Turnitin, Originality.ai, and Grammarly AI Detector
2. **Make it actually read as human** — scores the output across five authenticity dimensions (specificity, opinion, uncertainty, reader awareness, register consistency) and won't pass text that scores below 7/10

## Installation

```bash
git clone https://github.com/Gal3xy/ai-humanizer-skill.git ~/.claude/skills/ai-humanizer
```

## Trigger phrases

The skill activates automatically in Claude Code when you:

- Paste AI-generated text and ask to humanize or rewrite it
- Say "make this not sound like AI" or "this needs to sound more human"
- Ask to pass a specific detector: Turnitin, GPTZero, Originality.ai, Grammarly
- Say "de-AI this", "make this less robotic", "reduce my AI score"
- Ask Claude to rewrite something that was AI-generated

## How the process works

**8-step pipeline:**

1. **Read the room** — identify format, audience, voice, and register before touching a word
2. **Vocabulary detox** — strip kill-list words with specific replacements; catch verb inflation and lexical rotation
3. **Structural detox** — remove argument templates, hollow scope claims, bureaucratic list formatting, and transition patterns
4. **Rhythm reconstruction** — apply the burstiness formula to vary sentence length within every paragraph
5. **Authenticity injection** — score across five dimensions; add specificity, opinion, uncertainty, and reader awareness until the output hits 7/10
6. **Punctuation pass** — cap em dashes, reduce semicolons, remove bold overuse
7. **Dual-pass calibration** — Detector Pass (technical signals) then Reader Pass (would a person write this?) run separately
8. **Delivery check** — 14-point checklist before output

## What makes it different

**Detector-specific targeting.** GPTZero, Turnitin, Originality.ai, and Grammarly each weight signals differently. The skill maps which fixes matter most for each one.

**Authenticity scoring.** A 5-dimension 10-point score checks that the output actually reads as human — not just that it passes a machine. Text below 7/10 doesn't ship.

**Verb inflation detection.** AI replaces simple verbs ("is", "has") with elevated substitutes ("serves as", "boasts", "stands as") as a training artifact. This is caught and reversed.

**Lexical rotation detection.** AI cycles synonyms to avoid repetition — a statistical habit that trained readers spot immediately. The skill flags rotation clusters and consolidates to one word.

**Model fingerprinting.** ChatGPT, Claude, Gemini, and GPT-5+ have distinct output patterns. Knowing the source model sharpens the cleanup.

**Dual-pass calibration.** A Detector Pass and a Reader Pass run separately — they catch different failure modes and can't be merged into one read without missing things.

## File structure

```
ai-humanizer-skill/
├── SKILL.md                  # Full 8-step process and all frameworks
└── references/
    ├── kill-list.md          # 7-tier kill list organized by severity and model source
    └── examples.md           # Before/after rewrites across 6 formats with calibration notes
```

## Register support

Academic essays, LinkedIn posts, blog posts, business emails, news articles, technical documentation, and creative writing — each with calibrated contraction level, formality, opinion presence, and specificity expectations.
