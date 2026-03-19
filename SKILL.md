---
name: ai-humanizer
description: >
  Rewrites AI-generated text to sound authentically human — avoiding AI detector flags from tools like GPTZero, Turnitin, Originality.ai, and Grammarly AI Detector. Use this skill any time the user wants to humanize, de-AI, rewrite, or 'pass' AI-generated text, or when they ask to make text sound more natural, bypass AI detection, reduce AI score, or make writing sound like a real person wrote it. Also trigger when users say things like 'make this not sound like AI,' 'can you rewrite this so it passes Turnitin,' or 'this needs to sound more human.' Always use this skill before producing any humanized output — even for short passages.
---

# AI Humanizer Skill

Rewrites AI-generated text so it reads as authentic human writing — bypassing AI detectors and resonating naturally with human readers.

## How AI Detectors Work (What You're Defeating)

Detectors flag text using two core signals:
1. Perplexity — how predictable the next word is. AI text is too predictable. Human text surprises.
2. Burstiness — how much sentence length and structure vary. AI has low burstiness (uniform sentences). Human text fluctuates wildly.

They also scan for: banned vocabulary, structural fingerprints (formulaic openings, bullet-heavy structure, meta-commentary), punctuation patterns (em dash overuse, over-perfect grammar), tone homogeneity (too neutral, no personality, no opinions).

## Step-by-Step Humanization Process

### Step 1 — Understand Context First
Before rewriting, identify: purpose (academic essay? LinkedIn? blog? email?), audience (formal or casual?), voice (first/third person? brand tone?), desired reading level (aim Flesch 60–70 for most online content). If unclear, ask the user one concise question before proceeding.

### Step 2 — Vocabulary Detox (Kill List Pass)
Strip or replace ALL flagged words. See references/kill-list.md for the full list.
Core rule: if a word would make a human say 'that sounds like ChatGPT' — kill it.

Quick replacements (never use the left column):
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

Also strip:
- Filler openers: 'In today's ever-evolving world...', 'It is important to note that...', 'In the realm of...'
- Hollow closers: 'In conclusion...', 'In summary...', 'In essence...', 'Ultimately...'
- Sycophantic openers: 'Certainly!', 'Great question!', 'Absolutely!'
- Meta-commentary: 'In this article, we will explore...', 'As we discussed earlier...'
- Balanced-argument hedges: 'On one hand... on the other hand...' (pick a side)
- Corporate speak: synergy, ecosystem, paradigm shift, value proposition, thought leader

### Step 3 — Sentence Structure (Burstiness Fix)
This is the most powerful humanization lever. Rule: no two adjacent sentences should be the same length or structure.

Apply this rhythm formula across every paragraph:
Long sentence (20–30 words) → Short sentence (4–8 words) → Medium sentence (12–18 words) → Fragment or question.

Structural variety toolkit:
- Fragments: 'Not a bad start.' / 'Especially now.'
- Questions: 'But what does that actually mean?'
- Em dash (sparingly — max 1 per 300 words): use for genuine parenthetical drama, not as connector crutch
- Starting with conjunctions: 'And that's where it gets interesting.' / 'But here's the problem.'
- Short paragraph punches: a single sentence as its own paragraph.
- Contractions everywhere they fit: don't, it's, they're, won't, you've, we're

### Step 4 — Inject Humanity
Add at least one of these per 300 words of output:
1. Personal pronoun anchor: 'I've seen this go wrong when...' / 'You'll notice...'
2. Concrete specifics over abstractions: replace 'many studies' with 'three 2024 studies from Stanford'; replace 'significant improvement' with 'a 34% jump in 6 months'
3. Rhetorical question: 'So why does this matter?'
4. Mild opinion or stance: 'Honestly, most of the advice out there gets this wrong.'
5. Informal register dip: 'Here's the thing.' / 'Let's be real.' / 'Here's what's wild:'
6. Analogy from everyday life: not 'the complex interplay of factors' but 'it's like trying to bake bread while the oven keeps changing temperature'

### Step 5 — Structural Fixes
Paragraph variety: mix lengths (1 sentence, 3 sentences, 5 sentences). No more than 3 bullet points without a prose paragraph break. Avoid parallel-structure lists.

Transition replacements:
- Furthermore → Also / And / On top of that
- Moreover → What's more / Plus
- In addition → There's also the fact that
- Therefore → So / Which means
- However → But / That said / Still
- Consequently → As a result / So
- It is worth noting that → Worth mentioning:

Avoid: starting every paragraph with a transition word, identical sentence openings, 'Not just X, but Y', 'It isn't X, it's Y', 'This is where X comes in', third person universal ('One must consider...' → use 'you' or 'I')

### Step 6 — Punctuation Cleanup
- Em dashes: max 1 per 300 words
- Semicolons: use sparingly, break into two sentences when in doubt
- Exclamation marks: avoid unless genuinely warranted, max 1 per entire piece

### Step 7 — Final Quality Check
Before delivering output, verify:
- No words from the kill list appear
- Sentence lengths vary significantly across every paragraph
- No two adjacent paragraphs have the same structure
- At least one human element per 300 words
- Contractions used where appropriate
- Zero meta-commentary
- Zero hollow closers
- Em dash count ≤ 1 per 300 words
- Tone matches stated purpose
- Text reads naturally aloud

## Output Format
Deliver the rewritten text directly without preamble. For longer texts (500+ words), optionally flag 2–3 specific changes made.

## Register Guide
- Academic essay: low contractions, high formality, very low personal voice
- LinkedIn post: medium contractions, medium formality, high personal voice
- Blog post: high contractions, low-medium formality, high personal voice
- Business email: medium contractions, medium-high formality, low personal voice
- News article: low contractions, high formality, no personal voice
- Creative writing: very high contractions, low formality, very high personal voice

## Reference Files
- references/kill-list.md — Full categorized list of AI-flagged words and phrases
- references/examples.md — Before/after paragraph rewrites across different contexts
