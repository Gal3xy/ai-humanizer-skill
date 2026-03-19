# Kill List — Full Reference

This file is the complete vocabulary and pattern reference for the AI Humanizer skill. Organized by tier (severity) and model source where relevant.

---

## Tier 1 — Immediate Flags (Always Replace, No Exceptions)

These appear so consistently in AI output that a single instance can flag a passage. No context saves them.

| Word / Phrase | Replace With |
|---|---|
| delve | look into, dig into, explore, examine |
| tapestry | mix, blend, picture, combination |
| realm | field, area, space, world |
| meticulous(ly) | careful(ly), thorough(ly), precise(ly) |
| testament to | proof of, evidence that, shows that |
| in today's ever-evolving world | [rewrite with specific context or delete] |
| in the realm of | in [specific field] |
| Certainly! | [never use as opener] |
| Absolutely! | [never use as opener] |
| pivotal | key, central, critical, turning-point |
| multifaceted | complex, layered, multiple-sided |
| nestled | sitting, located, set in |
| it is important to note | [just say the thing] |
| paramount | most important, top priority |
| embark | start, set out, begin |
| beacon | guide, model, example |
| tapestry | mix, picture, blend |

---

## Tier 2 — High-Frequency AI Vocabulary (Replace When Present)

These don't flag on their own but cluster heavily in AI output. Two or more in a paragraph is a signal.

**Verbs:**
utilize, facilitate, commence, endeavour, harness, leverage, underscore, bolster, illuminate, garner, showcase, foster, navigate (metaphorical), amplify (metaphorical), cultivate (metaphorical), spearhead, pioneer (as verb)

**Adjectives:**
cutting-edge, groundbreaking, revolutionary, transformative, vibrant, intricate, commendable, invaluable, comprehensive, robust, seamless(ly), impactful, breathtaking, renowned, unparalleled, multifaceted, meticulous, pivotal

**Nouns:**
landscape (metaphorical), ecosystem (metaphorical), paradigm, synergy, thought leader, stakeholder, nuance (when vague), tapestry, journey (metaphorical), blueprint, cornerstone, foundation (metaphorical)

**Replacements — pick the most accurate option in context:**
- utilize → use
- facilitate → help, support, make easier
- harness → use, tap into
- leverage → use, take advantage of
- bolster → strengthen, support, boost
- illuminate → show, reveal, make clear
- showcase → show, display, demonstrate
- garner → get, earn, draw
- foster → build, develop, grow
- underscore → show, highlight, point to
- commendable → impressive, solid, worth noting
- robust → strong, reliable, solid
- seamlessly → smoothly, without friction
- groundbreaking → significant, new, notable
- transformative → major, meaningful, big shift

---

## Tier 3 — Structural Patterns (Rewrite the Whole Construction)

These are harder to spot because they're not single words — they're sentence shapes and paragraph structures.

### Hollow openers (delete or rewrite from scratch):
- "In today's fast-paced world..."
- "In the ever-evolving landscape of..."
- "As we navigate the complexities of..."
- "In the age of [X], it has never been more important to..."
- "Whether you're a [X] or a [Y]..."
- "At its core, [topic] is about..."
- "In a world where..."
- "[Topic] has become increasingly [adjective] in recent years..."

### Hollow closers (delete entirely):
- "In conclusion, ..."
- "In summary, ..."
- "In essence, ..."
- "Ultimately, ..."
- "To sum up, ..."
- "As we have seen, ..."
- "It is clear that ..."
- "The future looks bright..."
- "Exciting times lie ahead..."
- "As we move forward..."
- "By doing so, we can [vague aspiration]..."

### Meta-commentary (delete entirely):
- "In this article / essay / post, we will explore..."
- "As mentioned earlier / above..."
- "This section will cover..."
- "Before we dive in..."
- "Let's explore each of these in turn."
- "Now that we've covered X, let's move on to Y."

### Chatbot artifacts (delete entirely):
- "I hope this helps"
- "Would you like me to expand on any section?"
- "Feel free to ask if you have questions"
- "Of course!"
- "Great question!"
- "You're absolutely right!"
- "As an AI language model..."
- "I'd be happy to..."
- "Certainly, I can help with that"

### Knowledge-cutoff hedges (delete or rewrite):
- "as of my last update"
- "while specific details are limited"
- "based on my training data"
- "I don't have real-time access to..."

---

## Tier 4 — Verb Inflation

AI replaces flat, accurate verbs with elevated alternatives to sound more authoritative. This is a statistical training artifact — the model learned that formal writing uses complex constructions. Reverse it.

| AI phrase | Replace with |
|---|---|
| serves as | is |
| stands as | is |
| acts as | is / works as |
| functions as | works as / is |
| boasts | has |
| features (meaning has) | has |
| marks (meaning is) | is |
| represents (meaning is) | is |
| constitutes | is / makes up |
| embodies | is / shows |
| exemplifies | shows, is a good example of |

---

## Tier 5 — Argument Templates

AI defaults to common rhetorical templates from training data. These produce structurally identical arguments regardless of topic.

**Three-point structure overuse:** Every argument broken into exactly three numbered or bulleted points. Break this by using two, four, or leaving points unnumbered and flowing.

**Contrast stacking:**
- "Not only X, but also Y"
- "It isn't X, it's Y"
- "Not just X, but Y"
- "It goes beyond X — it's about Y"
Rewrite: take a position directly. If contrast is needed, use once max.

**Announcement constructions:**
- "This is where X comes in"
- "X is more than just Y; it's Z"
- "The answer lies in..."
- "That's exactly what X does"
Rewrite: skip the announcement, state the point.

**Hollow scope claims** — scope gestures that add no information:
- "from beginners to experts" → specify who actually benefits
- "from startups to Fortune 500 companies" → name the relevant scale
- "across all industries" → name the relevant industries
- "for everyone" → say who specifically
- "in today's world" → say when specifically

**Balanced-view hedging:** AI defaults to presenting "both sides" even when one side is clearly right or when the topic doesn't call for false balance. Take a position.

---

## Tier 6 — Punctuation Fingerprints

| Pattern | Fix |
|---|---|
| Em dash overuse | Max 1 per 300 words |
| Semicolons as default connector | Use a full stop instead |
| Bold on every key phrase | Bold for genuine emphasis only, rarely |
| Exclamation mark frequency | Max 1 per entire piece |
| Parallel bullet structure with bold labels | Convert to prose or plain bullets |

---

## Tier 7 — Lexical Rotation

AI is statistically penalized for repeating words across a passage, so it cycles synonyms to maintain variety. This produces an unnatural "elegant variation" that trained readers detect immediately.

**Signs of lexical rotation:**
- A concept described as "significant" in paragraph 1, "notable" in paragraph 2, "considerable" in paragraph 3, "meaningful" in paragraph 4
- A person or organization referred to by different noun phrases in alternating sentences with no reason for the variation

**Fix:** pick the most accurate word and use it. Repetition is human. Writers repeat words because they mean the specific thing that word means — not because they ran out of synonyms.

---

## Model-Specific Vocabulary Flags

Use these if the source model is known:

**ChatGPT (GPT-4o):**
delve, tapestry, realm, testament to, pivotal, multifaceted, meticulous, certainly, absolutely, groundbreaking, navigate (as metaphor), the intersection of, foster, nuanced approach

**Claude (Anthropic):**
I'd be happy to, I'd love to, certainly, nuanced, comprehensive, straightforward, robust, dive into (metaphor), it's worth noting, importantly, at its core, in many ways

**Gemini:**
Let's explore, dive into, vibrant, showcasing, highlighting, fostering, innovative solutions, certainly, of course, discover, exciting

**GPT-5+:**
Pronounced lexical rotation; heavier semicolons; over-formal academic constructions; fewer em dashes than GPT-4o but more than human baseline

---

## Context-Dependent Words

These appear in genuine human writing. Don't blindly replace:

- **keen** — common in British and Australian writing
- **crucial** — acceptable in urgent, high-stakes contexts
- **insights** — overused in business but still used by humans
- **furthermore** — acceptable once per document in formal writing
- **indeed** — fine in formal British register
- **innovative** — overused but not always AI
- **significant** — fine; only flag when rotating with synonyms
