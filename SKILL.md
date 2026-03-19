---
name: ai-humanizer
description: >
  Rewrites AI-generated text to sound authentically human. Trigger this skill whenever the user wants to humanize text, reduce an AI detection score, pass GPTZero, Turnitin, Originality.ai, or Grammarly AI Detector, or make writing sound like a real person wrote it. Also trigger for: 'make this not sound like AI', 'can you rewrite this so it passes [detector]', 'this needs to sound more human', 'de-AI this', 'make this less robotic', or any request to rewrite AI-generated content. Always invoke this skill before producing humanized output — even for a single paragraph. Do not attempt to humanize text without it.
---

# AI Humanizer Skill

Rewrites AI-generated text to read as authentic human writing — passing AI detectors and convincing human readers.

---

## The Two Failure Modes

Every bad humanization job fails in one of two ways:

**Failure Mode 1 — Technically clean, humanly dead.** The vocabulary passes a scanner but the writing has no point of view, no rhythm variation, no personality. It reads like a press release from a company that doesn't exist. Detectors miss it; humans don't.

**Failure Mode 2 — Has personality, trips the signals.** Voice is there but sentence lengths are uniform, flagged vocabulary slipped through, or the structure is too templated. Humans like it; detectors don't.

The goal is to pass both. This process fixes both, in order.

---

## How AI Detectors Actually Score Text

Detectors don't read for meaning — they score statistical properties:

**Perplexity score** — how surprising each word choice is given the words before it. LLMs pick high-probability next tokens by design. Human writers make low-probability choices constantly, through idiom, personal voice, and domain knowledge. Low perplexity = AI. Fix: introduce lexical unpredictability at the word level.

**Burstiness score** — the variance in sentence length across a passage. AI output has low variance (sentences cluster around 15–22 words). Human writing swings between 3-word punches and 35-word builds. Fix: the rhythm formula in Step 4.

**Vocabulary fingerprint** — a weighted scan against known AI word lists, cross-referenced with model-specific output patterns. Fix: the kill list in `references/kill-list.md`.

**Structural fingerprint** — pattern matching against common AI document structures: formulaic openers, parallel evidence lists, templated argument shapes, transition-heavy prose. Fix: Step 3.

**Detector-specific weightings:**
- **GPTZero** — perplexity and burstiness are the primary signals. Rhythm variation is the #1 fix here.
- **Turnitin** — weights structural fingerprints and academic formula patterns. Thesis-evidence-conclusion structure, parallel hedging, and passive voice chains are major flags.
- **Originality.ai** — heaviest vocabulary scanner of the major detectors. Kill list compliance is non-negotiable.
- **Grammarly AI** — focuses on punctuation patterns and micro-style: em dash density, semicolon frequency, bolding patterns. Cleanup in Step 6 targets this specifically.

---

## The Process

### Step 1 — Read the Room

Before touching a word, establish:
- **Purpose** — what is this piece of writing trying to do? (inform, persuade, connect, instruct)
- **Format** — academic essay, LinkedIn post, blog, email, report, creative writing?
- **Audience** — who reads this and what do they expect?
- **Voice** — first person, third person, brand voice, anonymous?

Use the Register Guide at the bottom to calibrate tone. If any of this is ambiguous, ask the user one question before proceeding. Getting this wrong means rewriting in the wrong direction.

---

### Step 2 — Vocabulary Detox

Run every sentence through the kill list in `references/kill-list.md`. The quick replacements below cover the most common offenders — the full list is in the reference file.

**Core rule:** if reading the word aloud would make someone think "ChatGPT wrote this" — replace it.

**Immediate replacements:**
- delve → look into, dig into, explore
- tapestry → mix, blend, picture
- realm → area, field, world
- utilize → use
- facilitate → help, support, make easier
- commence → start, begin
- endeavour → effort, attempt, try
- multifaceted → complex, layered
- pivotal → key, critical, central
- paramount → most important, top priority
- meticulous → careful, thorough
- commendable → impressive, solid
- cutting-edge → new, latest, current
- testament to → proof of, shows that
- underscore → highlight, show
- leverage → use, take advantage of
- seamlessly → smoothly
- harness → use, tap into
- groundbreaking → significant, new
- transformative → major, meaningful
- vibrant → lively, busy, rich
- embark → start, set out
- navigate (metaphor) → handle, deal with, work through
- bolster → strengthen, support
- illuminate → show, reveal, make clear
- showcase → show, demonstrate
- garner → get, earn
- foster → build, develop, grow

**Strip entirely:**
- Filler openers: "In today's world...", "It is important to note...", "In the realm of..."
- Hollow closers: "In conclusion...", "In summary...", "In essence...", "Ultimately..."
- Chatbot openers: "Certainly!", "Absolutely!", "Great question!"
- Chatbot closers: "I hope this helps", "Feel free to ask", "Let me know if you'd like me to expand"
- Meta-commentary: "In this piece, we will explore...", "As discussed above..."
- Hedging artifacts: "as of my last update", "based on available information"
- Corporate filler: synergy, paradigm shift, value proposition, thought leader, ecosystem (metaphorical)

**Verb inflation** — AI replaces flat, accurate verbs with elevated ones to sound more authoritative. It's a statistical habit from training on formal writing. Reverse it:
- "serves as" → is
- "stands as" → is
- "acts as" → is / works as
- "boasts" → has
- "features" (meaning has) → has
- "marks" (meaning is) → is
- "represents" (meaning is) → is
- "functions as" → works as / is

**Lexical rotation** — AI is statistically penalized for repeating words, so it cycles synonyms: "significant / notable / considerable / meaningful / substantial" used interchangeably throughout a piece. This pattern reads as unnatural because real writers repeat words without anxiety. Identify rotating synonym clusters and pick one word. Use it consistently.

---

### Step 3 — Structural Detox

Vocabulary alone isn't enough. These structural patterns trip detectors and human readers independently.

**Argument templates to break:**
- The three-point structure — AI defaults to three because it's the most common rhetorical template in training data. Use two points, four points, or don't number them at all.
- "Not only X, but Y" / "It isn't X, it's Y" / "Not just X, but Y" — these contrast constructions read as manufactured. Pick a position directly.
- "X is more than just Y; it's Z" — collapse it. Just say Z.
- "This is where X comes in" — skip the announcement. Say what X does.
- "The answer lies in..." — you have the answer; give it.
- Back-to-back contrast stacking: "Not for A. Not for B. But for C." Once reads as intentional. Twice reads as AI.

**Hollow scope claims** — phrases that gesture at breadth without adding information. Replace with something specific or cut entirely:
- "from beginners to experts" → who specifically benefits?
- "from startups to Fortune 500 companies" → what company size actually matters here?
- "across all industries" → name the relevant industries
- "for everyone" → who is this actually for?

**Bureaucratic list structure** — AI over-organizes information by tagging every bullet point with a bold category label and colon. This fingerprint is strong and consistent. Convert to prose or plain bullets without labels.

**Other formatting tells:**
- Title Case In Every Heading → use sentence case
- Emojis in headings or bullets (outside of casual social contexts)
- Every section ending with a sentence that transitions to the next section
- Parallel evidence: citing exactly three sources or examples for every claim

**Transition replacements:**
- Furthermore → Also, And, On top of that
- Moreover → What's more, Plus
- In addition → There's also
- Therefore → So, which means
- However → But, That said, Still
- Consequently → As a result, So
- It is worth noting → Worth mentioning

Don't start every paragraph with a transition word. It creates a cadence that reads as templated.

---

### Step 4 — Rhythm Reconstruction

This is the highest-impact fix for burstiness scores. A single paragraph with uniform sentence length will flag regardless of vocabulary.

**The rule:** no two adjacent sentences should be the same length or structural type.

**The rhythm formula — cycle through this across every paragraph:**

> Long sentence that builds context, adds detail, and moves toward a point (20–30 words). Short punch (4–8 words). Medium sentence that lands something (12–18 words). Fragment. Question?

**Tools for variety:**
- Fragments: "Not ideal." / "Especially at scale." / "Worth knowing."
- Sentence-opening questions: "So what actually changes?" / "But why does this matter?"
- Conjunction openers: "And that's the part most people miss." / "But it doesn't stop there."
- Single-sentence paragraphs — used once per section for impact.
- Contractions wherever they don't feel forced: don't, it's, they're, won't, you've, we're, I'd

**Paragraph length variation:** rotate between 1-sentence, 3-sentence, and 5-sentence paragraphs. Never run more than 3 bullet points without breaking back to prose.

---

### Step 5 — Authenticity Injection

Text can pass the structural and vocabulary checks and still read as hollow. This step adds the markers that signal a real person wrote it.

Rate yourself on these five dimensions before finalizing (aim for at least 7/10 total):

**1. Specificity (0–2)**
Replace abstractions with concrete details. "Many companies" → "Three companies I've worked with." "Significant improvement" → "37% drop in support tickets over 90 days." "Recent research" → "A 2024 University of Michigan study of 1,400 participants."

**2. Opinion (0–2)**
Real writers have a point of view. At least once per 300 words: "Honestly, most advice on this gets it backwards." / "I think this overstates the problem." / "The better question is why we accepted this for so long."

**3. Uncertainty (0–2)**
AI writes with false confidence. Humans hedge naturally: "I'm not sure this fully holds up, but..." / "The data here is messier than it looks." / "Take this with appropriate skepticism."

**4. Reader awareness (0–2)**
Write toward the person reading, not toward the topic: "You'll notice this..." / "If you've tried this before, you already know..." / "This probably sounds obvious, but in practice it rarely is."

**5. Register consistency (0–2)**
Mixing formal and casual isn't a problem — inconsistency within a register is. Pick a lane and stay in it. A blog post that shifts from conversational to academic mid-paragraph reads as stitched together.

---

### Step 6 — Punctuation Pass

- **Em dashes:** cap at 1 per 300 words. Overuse is a Claude fingerprint in particular.
- **Semicolons:** default to a full stop instead. Semicolons in informal writing are a flag.
- **Exclamation marks:** max 1 for the entire piece, only if genuinely warranted.
- **Bold text:** use for real emphasis only, not to highlight every key phrase. Bold-everything is an AI formatting habit.

---

### Step 7 — Dual-Pass Calibration

Before delivering, run two distinct passes. They catch different things.

**Pass 1 — Detector Pass**
Read purely for technical signals. Ignore meaning. Ask:
- Does sentence length vary significantly within each paragraph?
- Would any sentence be the statistically obvious next sentence given the previous one?
- Is there any vocabulary from the kill list?
- Does the structure match any common AI template?
Fix anything that fails. This pass is about the machine.

**Pass 2 — Reader Pass**
Read as if you've never seen this topic before. Ask:
- Would a person actually write this sentence?
- Is there at least one moment of real opinion, specific detail, or acknowledged uncertainty?
- Does anything feel like it was written to sound correct rather than to communicate?
- Would reading this aloud feel natural or slightly robotic?
Fix anything that fails. This pass is about the human.

The two passes catch different failures. Don't merge them into one read.

---

### Step 8 — Delivery Check

Before output:
- [ ] No kill-list vocabulary remains
- [ ] No verb inflation ("serves as", "stands as", "boasts")
- [ ] No lexical rotation (synonym cycling)
- [ ] Sentence length varies within every paragraph
- [ ] No three-point argument templates
- [ ] No hollow scope claims
- [ ] No bureaucratic list structure (bold-label + colon bullets)
- [ ] No hollow openers or closers
- [ ] No chatbot artifacts
- [ ] Em dash count ≤ 1 per 300 words
- [ ] Authenticity score ≥ 7/10 across the five dimensions
- [ ] Tone matches register guide
- [ ] Both calibration passes complete

---

## Output Format

**Short text (under 300 words):** deliver the final rewrite directly, no preamble.

**Long text (300+ words):**

```
[Rewritten text]

Calibration notes:
- Detector pass: [1–2 things fixed]
- Reader pass: [1–2 things added or changed]
- Register: [what register this was written to]
```

Keep calibration notes brief. They're for the user's reference, not a performance of effort.

---

## Register Guide

| Format | Contractions | Formality | Opinion | Specificity |
|---|---|---|---|---|
| Academic essay | Low | High | Very low | High (citations) |
| LinkedIn post | Medium | Medium | High | Medium |
| Blog post | High | Low–medium | High | High |
| Business email | Medium | Medium–high | Low | Medium |
| News article | Low | High | None | Very high |
| Creative writing | Very high | Low | Very high | High (sensory) |
| Technical docs | Low | High | Low | Very high |

---

## Model Fingerprints

Knowing the source model targets the cleanup. If the user identifies the source, use this:

**ChatGPT (GPT-4o):** "Certainly!" / "Absolutely!" openers, high em dash density, delve/tapestry/realm/testament cluster, three-point arguments on every topic, balanced-view hedging regardless of whether balance is warranted.

**Claude (Anthropic):** "I'd be happy to..." opener, comma-heavy long sentences, heavy em dash use as a connector (not emphasis), bureaucratic bold-label bullet lists, over-structured responses with headers for everything.

**Gemini:** Bullet-heavy, emojis in structure, "Let's explore..." / "Dive into...", conversational framing that collapses into templates, inconsistent register (too casual then suddenly formal).

**GPT-5+:** Fewer em dashes, heavier semicolons, pronounced lexical rotation (synonym cycling), over-formal in academic or professional registers even when the context doesn't call for it.

If the source is unknown, run the vocabulary pass — the kill list has model-specific flags in `references/kill-list.md`.

---

## Reference Files

- `references/kill-list.md` — Full kill list organized by tier and model source, with replacements
- `references/examples.md` — Full before/after rewrites across six formats showing both calibration passes
