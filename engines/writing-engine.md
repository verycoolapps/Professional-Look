# WRITING ENGINE
## Original Content Creation System

**Module:** `engines/writing-engine.md`
**Loaded by:** CREATE task class
**Dependencies:** `core/professional-standards.md`, `engines/tone-intelligence.md`, `reference/writing-patterns.md`

---

## PURPOSE

The Writing Engine handles original content creation — producing finished professional content from a brief, an idea, a context description, or a blank request. It does not rewrite existing text (that is `engines/rewriting-engine.md`). It starts from scratch and produces production-ready output.

---

## INPUT PARSING

Before writing a single word, extract the following from the user's request:

### Required Inputs (extract or request)
1. **Platform** — Where will this content live? (LinkedIn, Instagram, etc.)
2. **Objective** — What should this content achieve? (See: `core/decision-engine.md` objective taxonomy)
3. **Audience** — Who is reading this? Role, industry, relationship to author

### Strongly Preferred Inputs (extract or infer)
4. **Tone profile** — Which of the nine profiles? (See: `engines/tone-intelligence.md`)
5. **Key message** — The one idea this content must communicate
6. **Specific details** — Numbers, names, dates, outcomes, examples that can make this concrete

### Optional Inputs (use if provided, skip if not)
7. **Target length** — Short, medium, long, or specific character count
8. **Voice samples** — Previous content from the user that demonstrates their natural voice
9. **Constraints** — Topics to avoid, points that must be included, sensitivities

### Minimum Viable Brief
If only platform and objective are available, proceed. Inform the user that output will improve with more specific inputs, then deliver the best possible work with what exists.

---

## BRIEF EXTRACTION TECHNIQUE

For a vague request like "write me a LinkedIn post about leadership":

**Extract:**
- Platform: LinkedIn (explicit)
- Topic: Leadership (explicit but vague — narrow it)
- Objective: Infer from tone and context. Default: BUILD AUTHORITY
- Tone: Infer from user's history or default to Warm Professional

**Narrow the topic:**
The best content is not "about leadership" — it is about one specific observation, story, or principle related to leadership. Ask internally: what is the angle?

Angles for "leadership" on LinkedIn:
1. A specific mistake I made and what it taught me
2. One counterintuitive thing I believe about leadership
3. A decision I had to make alone and how I made it
4. What leadership looks like in practice (not what it sounds like in books)
5. The thing nobody says about being in charge

Select the angle that is most specific, most original, and most likely to produce content that sounds like a real human rather than a leadership content generator.

---

## STRUCTURAL SCAFFOLDING

Before writing, select the appropriate structural pattern from `reference/writing-patterns.md`.

### Pattern selection guide:
| Content Objective | Recommended Pattern |
|---|---|
| Share expertise | Insight-First or Authority Stack |
| Tell a story | Story Arc |
| Make an announcement | Announcement Frame |
| Share achievement subtly | Quiet Flex |
| Drive engagement | Magnetic Hook |
| Create a thread | Thread Spine |
| Deliver executive message | Executive Brief |

---

## HOOK WRITING

The hook is the first one to two lines. It determines whether the reader continues. Everything else can be brilliant — if the hook fails, it does not matter.

### Hook taxonomy

**Type 1: Contradiction**
Open with something that contradicts expectation.
> "The best advice I ever got was to do nothing."

**Type 2: Surprising Fact**
Open with a number, statistic, or finding that is not obvious.
> "Eighty percent of enterprise deals we lost in Q1 were lost before we ever sent a proposal."

**Type 3: Bold Opinion**
Open with a position most professionals in the space would not take publicly.
> "The obsession with productivity culture is why most teams never get anything important done."

**Type 4: Specific Scenario**
Open in the middle of a story or situation.
> "Three years ago, I told my board we needed to cut 40% of the product roadmap. They told me to come back with a better answer."

**Type 5: Direct Question (specific)**
A question that the intended reader wants to answer, not a hollow prompt.
> "How many enterprise accounts did you lose last year because of onboarding, not the product?"

**What hooks must never do:**
- Start with "I'm excited/thrilled/honored..."
- Start with a rhetorical question the reader cannot answer ("Have you ever wondered what success feels like?")
- State the obvious ("Leadership is important in business.")
- Open with context before the point ("For the past fifteen years, I have been working in...")

---

## BODY DEVELOPMENT

### Principles
- One idea per paragraph
- Maximum four sentences per paragraph in social content
- Each paragraph must advance the piece — not repeat, not decorate
- If a paragraph can be removed without damaging the piece, remove it

### Body structures by objective

**BUILD AUTHORITY:**
Hook → Core insight → Supporting evidence (specific) → Implication for reader → Quiet close

**ANNOUNCE:**
What happened → Why it matters → What comes next → Optional: invitation to respond

**INSPIRE:**
Specific situation → What happened → What it revealed → What this means for the reader

**EDUCATE:**
Problem or question → Key insight → Evidence or example → How to apply

**ENGAGE:**
Contradiction or surprising point → Exploration → Your position → Specific invitation to reader's experience

---

## CTA FORMULATION

Not every piece needs a call to action. When it does, follow these rules:

**Principles:**
- A CTA must ask for something specific
- It must match the content's register — a CEO/Founder post does not end with "Drop a comment below!"
- It must offer the reader a reason to respond beyond just completing the author's engagement goals

### CTA by tone profile
| Tone Profile | CTA Style |
|---|---|
| CEO/Founder | No CTA or rhetorical close that invites thought, not engagement |
| Executive | Specific question tied to the content's core insight |
| Intellectual | Invite challenge to your position or additional evidence |
| Warm Professional | Genuine invitation to share related experience |
| Leadership | Encourage the reader to apply the principle and share what happens |
| Luxury/Premium | No CTA or elegant invitation without imperative language |
| Corporate | State the next action precisely if required |
| Crisis | State clearly what the organization will do next; do not ask for engagement |
| Diplomatic | Open the floor for perspective sharing without pressure |

---

## VOICE CONSISTENCY CHECK

After drafting, verify:
1. Read first sentence and last sentence — same voice?
2. Is there any sentence that breaks the established register?
3. Is the level of formality consistent throughout?
4. Is there any borrowed language from other sources without attribution?

---

## PLATFORM-LENGTH COMPLIANCE

Before finalizing, verify against platform specifications in `reference/platform-formats.md`.

| Platform | Typical Content Length |
|---|---|
| LinkedIn post | 150–300 words (optimal engagement); up to 700 for long-form |
| LinkedIn article | 800–2000 words |
| Instagram caption | 50–150 words optimal; max 2200 characters |
| X/Twitter tweet | Under 280 characters |
| X/Twitter thread | 5–20 tweets |
| TikTok caption | Under 150 characters |
| YouTube description | 200–500 words |
| Facebook post | 50–300 words |

---

## WRITING SEQUENCE

```
1. Extract brief → identify platform, objective, audience, tone
2. Narrow topic → select specific angle
3. Select structural pattern → from reference/writing-patterns.md
4. Write hook → apply hook taxonomy
5. Develop body → one idea per paragraph
6. Formulate close/CTA → match tone profile
7. Voice consistency check
8. Platform-length compliance check
9. Anti-slop scan → engines/anti-ai-slop-engine.md
10. Quality score → core/quality-control.md
11. Deliver
```

---

## FAILURE MODES

| Failure | Signal | Fix |
|---|---|---|
| Generic content | No specific details; could be from anyone | Ask for one concrete example, number, or story |
| Tone mismatch | Opening and closing feel different | Re-read with tone profile in mind; align closing |
| Weak hook | First line is context-setting, not compelling | Apply hook taxonomy; replace first line entirely |
| Over-long for platform | Content works but wrong length | Trim to platform spec; prioritize the strongest sentences |
| Missing point of view | Content describes but does not take a position | Add one declarative statement that is the author's actual position |

---

## RELATIONSHIP TO OTHER MODULES

- `core/decision-engine.md` — activates this engine and provides task parameters
- `engines/tone-intelligence.md` — provides the tone profile for execution
- `reference/writing-patterns.md` — provides structural scaffolding
- `engines/anti-ai-slop-engine.md` — mandatory review after drafting
- `core/quality-control.md` — gates delivery
