---
name: ai-humanizer
description: >
  Rewrites AI-generated text to sound authentically human — avoiding AI detector flags from tools like GPTZero, Turnitin, Originality.ai, and Grammarly AI Detector. Use this skill any time the user wants to humanize, de-AI, rewrite, or 'pass' AI-generated text, or when they ask to make text sound more natural, bypass AI detection, reduce AI score, or make writing sound like a real person wrote it. Also trigger when users say things like 'make this not sound like AI,' 'can you rewrite this so it passes Turnitin,' or 'this needs to sound more human.' Always use this skill before producing any humanized output — even for short passages.
---

# AI Humanizer Skill

Rewrites AI-generated text so it reads as authentic human writing — bypassing AI detectors and resonating naturally with human readers.

## What You're Actually Doing

Two goals, both matter:

1. **Defeat detectors** — GPTZero, Turnitin, Originality.ai, Grammarly AI Detector all use perplexity (word predictability) and burstiness (sentence length variation) as primary signals, plus vocabulary scanning and structural fingerprinting.

2. **Make it actually good** — Technically "clean" text can still read as dead. Soulless writing has no opinions, no rhythm, no acknowledgment that a human being wrote it. Avoiding AI patterns is only half the job.

Both checks happen before any output goes to the user.

---

## How Detectors Work (What You're Defeating)

**Primary signals:**
- **Perplexity** — AI text is too predictable. Models pick statistically likely next words. Human writers surprise. Introduce lexical unpredictability.
- **Burstiness** — AI sentences are uniform in length and structure. Human writing fluctuates wildly. This is the most powerful lever you have.

**Secondary signals:**
- Flagged vocabulary (kill list)
- Structural fingerprints: formulaic openers/closers, bullet-heavy structure, parallel lists, section headers, meta-commentary
- Punctuation patterns: em dash overuse, semicolons everywhere, over-perfect grammar
- Tone homogeneity: too neutral, no personality, no uncertainty, no opinions

**Detector-specific notes:**
- **Turnitin** — weights academic register heavily. Formulaic thesis structures, parallel evidence presentation, and hedging language are major flags.
- **GPTZero** — most sensitive to perplexity and burstiness. Sentence rhythm variation is the #1 fix.
- **Originality.ai** — strong vocabulary scanner. Kill list compliance is critical.
- **Grammarly AI** — focuses on structural and style fingerprints. Vary paragraph structure aggressively.

---

## Signs of Soulless Writing (Even If Technically Clean)

Passing detectors doesn't mean passing human readers. Before finalizing, check for:
- Every sentence the same length and structure
- No opinions, just neutral reporting
- No acknowledgment of uncertainty or mixed feelings
- No first-person perspective when appropriate
- No humor, no edge, no personality
- Reads like a Wikipedia article or press release

**How to add soul:**
- Have opinions. React to facts, don't just report them.
- Vary rhythm aggressively. Short punchy sentences. Then longer ones that build.
- Acknowledge complexity honestly. "This is impressive but also kind of unsettling" beats "This is impressive."
- Use "I" when it fits. "I keep coming back to..." signals a real person.
- Let some mess in. Tangents, asides, half-formed thoughts are human.
- Be specific about feelings. Not "this is concerning" but "there's something unsettling about it."

---

## The Process

### Step 1 — Understand Context First

Before rewriting, identify: purpose (academic essay? LinkedIn? blog? email?), audience (formal or casual?), voice (first/third person? brand tone?), desired reading level (aim Flesch 60–70 for most online content).

Use the Register Guide at the bottom to calibrate. If the context is ambiguous, ask one concise question before proceeding.

---

### Step 2 — Vocabulary Detox

Strip or replace ALL flagged words. See `references/kill-list.md` for the full categorized list.

**Core rule:** if a word would make a human reader think "that sounds like ChatGPT" — kill it.

**Quick replacements (never use the left column):**
- delve → look into, explore, dig into
- tapestry → mix, combination, blend
- realm → area, field, world
- utilize → use
- facilitate → help, support, enable
- commence → start, begin
- endeavour → effort, attempt, try
- multifaceted → complex, layered
- pivotal → key, critical, central
- paramount → most important, top priority
- meticulous → careful, thorough, detailed
- commendable → impressive, solid, worth noting
- cutting-edge → new, latest, modern
- revolutionary → new, game-changing (use sparingly)
- testament to → proof of, shows that
- underscore → highlight, show, point to
- leverage → use, take advantage of
- seamlessly → smoothly, without friction
- harness → use, tap into
- groundbreaking → significant, new
- transformative → big change, meaningful shift
- vibrant → lively, busy, rich
- beacon → guide, example, model
- embark → start, begin, set out
- navigate (metaphor) → handle, deal with, work through
- foster → build, develop, grow
- bolster → strengthen, support, boost
- illuminate → show, reveal, make clear
- showcase → show, display, demonstrate
- garner → get, earn, draw
- nestled → sitting, located, set

**Also strip:**
- Filler openers: "In today's ever-evolving world...", "It is important to note that...", "In the realm of..."
- Hollow closers: "In conclusion...", "In summary...", "In essence...", "Ultimately..."
- Sycophantic openers: "Certainly!", "Great question!", "Absolutely!"
- Meta-commentary: "In this article, we will explore...", "As we discussed earlier..."
- Chatbot artifacts: "I hope this helps", "Would you like me to expand on...", "Feel free to ask"
- Knowledge-cutoff hedges: "as of my last update", "while specific details are limited"
- Corporate speak: synergy, ecosystem (metaphorical), paradigm shift, value proposition, thought leader, stakeholder

**Copula avoidance — a subtle AI tell:** Replace false verbs that dress up "is/are/has" as something more important:
- "serves as" → is
- "stands as" → is
- "marks" (when meaning "is") → is
- "boasts" → has
- "features" (when meaning "has") → has
- "represents" (when meaning "is") → is

**Synonym cycling:** AI avoids repeating words by substituting synonyms. Humans repeat words naturally. If the text uses "significant", "notable", "considerable", and "meaningful" to describe the same type of thing, that's AI. Pick one word and use it consistently.

---

### Step 3 — Structural Pattern Removal

These patterns flag as AI even after vocabulary cleanup:

**Formulaic structures to rewrite:**
- "Not only X, but also Y" / "It isn't X, it's Y" / "Not just X, but Y" — pick a lane
- "This is where X comes in" — just say what X does
- "X is more than just Y; it's Z" — cut to Z
- "The answer lies in..." — just give the answer
- Rule of three: AI forces every argument into exactly three points. Break the pattern — use two, four, or leave it open-ended
- Balanced-argument hedges: "On one hand... on the other hand..." — take a side
- Negative parallelisms back-to-back: "Not just for A. Not just for B. But for C." — once is fine, twice is a tell

**Structural formatting tells:**
- Inline-header bullet lists: bold header + colon + explanation in every bullet point (this is a strong AI fingerprint — convert to prose or plain bullets)
- Title Case In Every Heading — use sentence case
- Emojis in headings or bullets
- Ending every section with a transition sentence to the next section
- Listing exactly three pieces of evidence for every claim

**False ranges:** "from startups to Fortune 500 companies", "from beginners to experts" — these rarely add meaning. Cut or replace with something specific.

**Transition replacements:**
- Furthermore → Also / And / On top of that
- Moreover → What's more / Plus
- In addition → There's also the fact that
- Therefore → So / Which means
- However → But / That said / Still
- Consequently → As a result / So
- It is worth noting that → Worth mentioning:
- Avoid starting every paragraph with a transition word

---

### Step 4 — Sentence Structure (Burstiness Fix)

The single most powerful lever for defeating perplexity and burstiness detectors.

**Rule:** no two adjacent sentences should be the same length or structure.

**Rhythm formula — apply across every paragraph:**
Long sentence (20–30 words) → Short sentence (4–8 words) → Medium sentence (12–18 words) → Fragment or question.

**Structural variety toolkit:**
- Fragments: "Not a bad start." / "Especially now."
- Questions: "But what does that actually mean?"
- Starting with conjunctions: "And that's where it gets interesting." / "But here's the problem."
- Short paragraph punches: a single sentence as its own paragraph
- Contractions everywhere they naturally fit: don't, it's, they're, won't, you've, we're

**Paragraph variety:** mix lengths (1 sentence, 3 sentences, 5 sentences). No more than 3 bullet points without a prose paragraph break. Avoid parallel-structure lists.

---

### Step 5 — Inject Humanity

Add at least one of these per 300 words:

1. **Personal pronoun anchor:** "I've seen this go wrong when..." / "You'll notice..."
2. **Concrete specifics:** replace "many studies" with "three 2024 studies from Stanford"; replace "significant improvement" with "a 34% jump in six months"
3. **Rhetorical question:** "So why does this matter?"
4. **Mild opinion or stance:** "Honestly, most of the advice out there gets this wrong."
5. **Informal register dip:** "Here's the thing." / "Let's be real." / "Here's what's wild:"
6. **Everyday analogy:** not "the complex interplay of factors" but "it's like trying to bake bread while the oven keeps changing temperature"
7. **Acknowledgment of uncertainty:** "I'm not sure this fully explains it, but..." / "The data is messy here."
8. **Specific emotional reaction:** not "this is concerning" but "there's something unsettling about the fact that..."

---

### Step 6 — Punctuation Cleanup

- **Em dashes:** max 1 per 300 words. They're a Claude fingerprint when overused.
- **Semicolons:** use sparingly. When in doubt, make two sentences.
- **Exclamation marks:** avoid unless genuinely warranted. Max 1 per entire piece.
- **Bold/italics:** don't bold every key phrase. Bold is for genuine emphasis, used rarely.
- **Curly quotes:** use straight quotes in casual/digital contexts if appropriate.

---

### Step 7 — Self-Audit Pass (Two-Pass Revision)

After completing the draft, do not deliver it yet.

Ask yourself: **"What still makes this obviously AI-generated?"**

Answer in brief bullets — be honest and specific. Look for:
- Any kill-list words that slipped through
- Paragraphs with uniform sentence length
- Any structural AI clichés still present
- Sections that feel neutral and reporterly but have no human voice
- Anything that would make a human reader think "ChatGPT wrote this"

Then revise based on those bullets. The self-audit catches what the checklist misses — it forces a fresh read with fresh eyes.

---

### Step 8 — Final Quality Check

Before delivering:
- [ ] No kill-list words remain
- [ ] Sentence lengths vary significantly across every paragraph
- [ ] No two adjacent paragraphs have the same structure
- [ ] At least one human element per 300 words
- [ ] Contractions used where appropriate
- [ ] Zero meta-commentary or chatbot artifacts
- [ ] Zero hollow closers
- [ ] Em dash count ≤ 1 per 300 words
- [ ] No inline-header bullet formatting
- [ ] No rule-of-three forcing
- [ ] No copula avoidance tells ("serves as", "stands as", "boasts")
- [ ] No synonym cycling
- [ ] Tone matches stated purpose and register
- [ ] Text reads naturally aloud

---

## Output Format

**For short texts (under 300 words):** Deliver the final rewrite directly.

**For longer texts (300+ words):** Use this format:

---
*[Draft rewrite]*

**Self-audit — remaining AI tells:**
- [bullet 1]
- [bullet 2]

*[Final rewrite after self-audit corrections]*

**Changes made:** [2–3 specific things you changed and why]

---

Always deliver the **final** version last. The self-audit draft is shown so the user can see the reasoning, not because it's acceptable output.

---

## Register Guide

| Format | Contractions | Formality | Personal Voice |
|---|---|---|---|
| Academic essay | Low | High | Very low |
| LinkedIn post | Medium | Medium | High |
| Blog post | High | Low–medium | High |
| Business email | Medium | Medium–high | Low |
| News article | Low | High | None |
| Creative writing | Very high | Low | Very high |

---

## Model-Specific Fingerprints

Knowing which model generated the text helps target the right tells:

- **ChatGPT (GPT-4o):** Opens with "Certainly!" or "Absolutely!", high em dash density, "delve/tapestry/realm/testament to", balanced-argument structure on every topic, rule-of-three everywhere
- **Claude (Anthropic):** Opens with "I'd be happy to..." or "I'd love to...", longer hedged sentences, heavy em dash and comma-clause use, inline-header bullet formatting
- **Gemini:** More conversational but over-structured, bullet-heavy, "Let's explore", "Dive into", emojis in headings
- **GPT-5+:** Fewer em dashes, more semicolons, still over-formal in academic contexts, synonym cycling is pronounced

---

## Reference Files

- `references/kill-list.md` — Full categorized list of AI-flagged words and phrases
- `references/examples.md` — Before/after rewrites with self-audit annotations across six contexts
