# 20 Rules of Formulating Knowledge for Spaced Repetition
*Dr. Piotr Wozniak*

---

## Rule 1: Do Not Learn If You Do Not Understand

**Principle:** Never memorize material you haven't comprehended first. Blind memorization produces fragile, useless knowledge.

- Learning without understanding is astronomically slow and produces near-zero value
- If material seems structured but you still don't grasp it, don't proceed — review it until you do
- Polluting your collection with misunderstood items wastes future repetition time

---

## Rule 2: Learn Before You Memorize

**Principle:** Build a mental overview of the whole before breaking it into individual cards.

- Read a full chapter or overview first to see how pieces fit together
- Only after the big picture is clear should you create individual Q&A pairs
- A single isolated fact is as useless as a single word in a foreign-language book

**Example:** Read about "how an internal combustion engine works" before creating cards like "What moves the pistons?"

---

## Rule 3: Build Upon the Basics

**Principle:** Start with simple models and layer complexity on top.

- The simpler the initial picture, the easier it is to comprehend and extend
- Do not skip "obvious" basics — they are cheap to learn and extremely costly to forget
- ~50% of repetition time goes to just 3–5% of material (usually the basics)
- Basics are easy to retain but each lapse on them cascades into larger failures

---

## Rule 4: Stick to the Minimum Information Principle

**Principle:** Each card should test exactly one atomic fact.

**Why simpler is better:**
- Simple items have only one recall path; complex items create interfering neural traces
- Each sub-item can be scheduled at its own optimal interval, saving total repetition time
- Complex items force unnecessarily frequent repetitions of all sub-items

**Bad (complex, wordy):**
```
Q: What are the characteristics of the Dead Sea?
A: Salt lake on the Israel-Jordan border. Lowest point on Earth's surface
   (~396m below sea level). 74km long. 7x saltier than the ocean (30% by
   volume). Density keeps swimmers afloat. Only simple organisms survive.
```

**Good (atomic):**
```
Q: Where is the Dead Sea located?
A: On the border between Israel and Jordan

Q: What is the lowest point on Earth's surface?
A: The Dead Sea shoreline

Q: How far below sea level is the Dead Sea?
A: ~400 meters

Q: How long is the Dead Sea?
A: ~70 km

Q: How much saltier is the Dead Sea than the ocean?
A: 7 times

Q: What is the salt content of the Dead Sea by volume?
A: 30%

Q: Why does the Dead Sea keep swimmers afloat?
A: High salt content increases water density

Q: Why is the Dead Sea called "Dead"?
A: Only simple organisms can survive its salinity
```

---

## Rule 5: Cloze Deletion Is Easy and Effective

**Principle:** Replace a key term or phrase with `[...]` to create a fill-in-the-blank card.

- Ideal for beginners struggling with the minimum information principle
- Fast to create from existing text
- Forms the basis of incremental reading techniques

**Bad (complex Q&A):**
```
Q: What was the history of Kaleida?
A: Funded $40M by Apple and IBM in 1991. Mission: multimedia programming
   language. Produced Script X after 3 years. Macromedia/Asymetrix captured
   the market. Closed 1995.
```

**Good (cloze deletions):**
```
Q: Kaleida was funded [...] by Apple and IBM in 1991.
A: $40 million

Q: Kaleida was funded $40M by [...] in 1991.
A: Apple and IBM

Q: Kaleida was funded $40M by Apple and IBM in [year].
A: 1991

Q: Kaleida's mission was to create a [...].
A: multimedia programming language

Q: Kaleida's multimedia language was called [...].
A: Script X

Q: Script X took [...] to produce.
A: three years

Q: Companies like [...] captured Kaleida's market while Script X was delayed.
A: Macromedia and Asymetrix

Q: Kaleida closed in [year].
A: 1995
```

---

## Rule 6: Use Imagery

**Principle:** Visual information is retained far better than verbal information.

- The brain's visual cortex is evolutionarily optimized — one image can encode thousands of words
- Graphics are especially powerful in: anatomy, geography, geometry, chemistry, history
- Weigh the cost of finding/creating images against the learning benefit
- Mind maps (Tony Buzan) leverage imagery to represent logical connections

**Example:**
```
Less effective:
Q: What African country lies between Kenya, Zambia, and Mozambique?
A: Tanzania

More effective:
Q: What country is highlighted on this map? [map image]
A: Tanzania
```

---

## Rule 7: Use Mnemonic Techniques

**Principle:** Use deliberate memory aids (peg lists, mind maps, vivid associations) for difficult items.

- Mnemonic techniques are learnable skills, not innate talent
- With practice, you'll only need them consciously for 1–5% of items; the rest becomes automatic
- **Warning:** Mnemonics speed up initial learning, but spaced repetition is still required for long-term retention
- Resources: Tony Buzan's books; search "mind maps," "peg lists," "mnemonic techniques"

---

## Rule 8: Graphic Deletion Is as Good as Cloze Deletion

**Principle:** Cover part of an image and ask the student to identify the hidden component.

- A single diagram can generate 10–20 cards (one per labeled region)
- Especially effective for: anatomy, geography, labeled diagrams
- The same source image is reused across all derived cards (efficient storage)

---

## Rule 9: Avoid Sets

**Principle:** Never ask "list all members of this set" — it's nearly impossible to retain reliably.

- Sets with more than 5 members are virtually un-memorizable without tricks
- Listing members in varying order each repetition destroys memory traces
- **Fix:** Convert sets into ordered enumerations, or better, into meaningful Q&A chains

**Bad (set):**
```
Q: What countries belong to the EU (2002)?
A: Austria, Belgium, Denmark, Finland, France, Germany, Greece, Ireland,
   Italy, Luxembourg, Netherlands, Portugal, Spain, Sweden, UK
```

**Good (meaningful chain):**
```
Q: Which country hosted the 1951 European Defence Community meeting?
A: France

Q: Which countries joined France in the 1952 Coal and Steel Community?
A: Germany, Italy, and the Benelux

Q: What countries make up the Benelux?
A: Belgium, Luxembourg, and the Netherlands

Q: Whose EU membership did de Gaulle oppose in the 1960s?
A: The UK's

Q: Which countries joined the EEC with the UK in 1973?
A: Ireland and Denmark

Q: Which country joined the EEC in 1981?
A: Greece

Q: Which countries joined the EEC in 1986?
A: Spain and Portugal

Q: Which countries joined the EU in 1995?
A: Austria, Sweden, and Finland
```

---

## Rule 10: Avoid Enumerations

**Principle:** Ordered lists are better than sets but still difficult — use overlapping cloze deletions to handle them.

- Enumerations are more reliable than sets (fixed order forces consistent recall)
- Use overlapping cloze deletions so adjacent elements reinforce each other
- Redundancy across overlapping items is acceptable (each item is still minimal)

**Bad:**
```
Q: What is the sequence of letters in the alphabet?
A: abcdefghijklmnopqrstuvwxyz
```

**Good (overlapping cloze):**
```
Q: What three letters does the alphabet begin with?
A: A, B, C

Q: A [...] [...] [...] E
A: B, C, D

Q: B [...] [...] [...] F
A: C, D, E

Q: C [...] [...] [...] G
A: D, E, F
```

**For poems:** Use overlapping cloze on stanza segments; only switch to cloze when you notice you're stumbling.

---

## Rule 11: Combat Interference

**Principle:** Similar items confuse each other. Actively detect and eliminate interference.

- Interference is the #1 cause of forgetting in large, mature collections
- It can arise between seemingly unrelated items and is hard to predict in advance
- Once spotted, fix immediately before it becomes a persistent failure

**Prevention strategies:**
- Make items as unambiguous as possible
- Apply the minimum information principle strictly
- Use examples, context cues, imagery, and emotional anchors to differentiate similar items
- Regularly review your most difficult/failed cards and rewrite them

---

## Rule 12: Optimize Wording

**Principle:** Reduce card text to the minimum needed to trigger the correct memory.

- Every extra word increases reading time and risks activating wrong associations
- Optimize iteratively — keep cutting until meaning would be lost

**Progressive optimization example:**
```
Worst:
Q: Aldus invented desktop publishing in 1985 with PageMaker. Aldus had little
   competition for years, and so failed to improve. Then Denver-based [...]
   blew past. PageMaker, now owned by Adobe, remains No. 2
A: Quark

Better:
Q: Aldus invented desktop publishing with PageMaker but failed to improve.
   It was soon outdistanced by [...]
A: Quark

Best:
Q: PageMaker lost ground to [...]
A: Quark
```

> The stripped context (ownership, year, location) is not lost — it belongs in *separate* cards if it matters to you.

---

## Rule 13: Refer to Other Memories

**Principle:** Anchor new memories to things you already know well.

- Using familiar concepts in the question reduces ambiguity and interference
- Builds a coherent, self-reinforcing knowledge structure
- Requires that the referenced memories are already solid (see Rule 3: basics first)

**Example:**
```
Prone to interference:
Q: derog. adj: shamelessly conscious of one's failings and asking in a begging way
A: cringing

Better (anchored to known words):
Q: derog. adj: shamelessly humble and supplicant
A: cringing
```

---

## Rule 14: Personalize and Provide Examples

**Principle:** Link items to your own life, experiences, and people you know.

- Personal references are highly resistant to interference
- They activate rich, pre-existing memory networks
- A private collection justifies highly personal, even idiosyncratic examples

**Example:**
```
Generic (interference-prone):
Q: What is a soft bed without arms or back?
A: divan

Personalized:
Q: What is a soft bed without arms or back? (like the one at Robert's parents)
A: divan
```

---

## Rule 15: Rely on Emotional States

**Principle:** Vivid, emotionally charged examples dramatically improve retention.

- Emotions are tightly coupled to memory encoding and retrieval
- Shocking, funny, or personally meaningful examples are far more memorable
- Avoid overusing the same emotional hook (creates its own interference)
- Ensure the emotional cue will be available when you need to recall the fact in real life

**Example:**
```
Harder:
Q: a light and joking conversation
A: banter

Easier:
Q: a light and joking conversation (e.g. Mandela and de Klerk in 1992)
A: banter
```

> One well-chosen example can reduce forgetting by 25× over 20 years.

---

## Rule 16: Context Cues Simplify Wording

**Principle:** Use tags, categories, or labels to establish domain context so you don't have to spell it out in every card.

- Context shifts the brain into the right mode before reading the question
- Prevents cross-domain interference (e.g., "GRE" meaning different things in biochemistry vs. education)
- Use consistent prefixes or tags (e.g., `bioch:`, `hist:`, `math:`)

**Example:**
```
Ambiguous (risks wrong context activation):
Q: What does GRE stand for in biochemistry?
A: glucocorticoid response element

Clear (context-labeled):
Q: bioch: GRE =
A: glucocorticoid response element
```

---

## Rule 17: Redundancy Does Not Contradict Minimum Information Principle

**Principle:** Representing the same knowledge from multiple angles is beneficial, not wasteful — as long as each individual card remains simple.

**Acceptable forms of redundancy:**

| Type | Description |
|------|-------------|
| **Active + passive** | Learn word pairs in both directions (e.g., `phone → telefono` AND `telefono → phone`) |
| **Reasoning cues** | Include the reasoning steps in the answer to reinforce problem-solving paths |
| **Derivation steps** | Break complex proofs/derivations into individually memorized steps |
| **Multiple representations** | Encode the same fact from different semantic angles for high-value knowledge |
| **Flexible responses** | Accept any valid synonym as correct (e.g., `blot / blob / blotch` for the same definition) |

---

## Rule 18: Provide Sources

**Principle:** Tag each card with its source so you can verify, update, and judge the reliability of knowledge.

- Real-world knowledge is often contradicted by other reputable sources
- Sources let you resolve conflicts and update outdated information
- Sources are metadata — do not include them as tested content unless recalling the source is itself the goal
- Consider reliability labels: `[unverified]`, `[contradicted by X]`, `[estimated]`

---

## Rule 19: Provide Date Stamping

**Principle:** Tag time-sensitive facts with when they were current.

| Knowledge type | Stability | Stamping approach |
|----------------|-----------|-------------------|
| Math, anatomy, logic | Stable | No stamp needed |
| Economic indicators, software APIs | Volatile | Stamp with year or version |
| Historical trends over time | Intrinsic timeline | Date is part of the answer |

- Update or retire cards when their facts become outdated
- For facts that change over time (e.g., GNP by year), the date becomes tested content

---

## Rule 20: Prioritize

**Principle:** You will always have more to learn than time allows. Prioritization determines the quality of your long-term knowledge.

**Prioritization layers:**

1. **Sources** — Allocate time across sources proportional to their value to you
2. **Extraction** — Don't memorize whole books; extract only what will impact your knowledge quality
3. **Formulation** — If accurate formulation takes seconds, do it now; if it requires research, import raw and refine later
4. **Item construction** — Put optional/explanatory content in parentheses; keep the critical answer front and center
5. **Retention level** — Assign higher retention targets to high-priority items
6. **During review** — Re-memorize changed items; reschedule, execute early, or dismiss items based on current priority

---

## Summary: The Core Insight

The first 16 rules all serve one purpose: **make memories simple**.

Simplicity → single recall path → consistent neural activation → durable retention.

| Problem | Primary rules to apply |
|---------|------------------------|
| Cards too hard to remember | 4 (minimize info), 5 (cloze), 12 (optimize wording) |
| Confusing similar cards | 11 (combat interference), 13 (refer to memories), 16 (context cues) |
| Abstract/unmemorable facts | 6 (imagery), 7 (mnemonics), 14 (personalize), 15 (emotion) |
| Long lists | 9 (avoid sets), 10 (avoid enumerations) |
| Cards becoming outdated | 18 (sources), 19 (date stamps) |
| Too much to learn | 20 (prioritize) |
| Cards memorized but not understood | 1 (understand first), 2 (learn first), 3 (basics first) |
