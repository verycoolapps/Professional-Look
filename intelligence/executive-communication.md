# EXECUTIVE COMMUNICATION
## CEO-Level Messaging Intelligence

**Module:** `intelligence/executive-communication.md`
**Loaded by:** Tasks requiring CEO, founder, or senior executive communication
**Dependencies:** `engines/tone-intelligence.md`, `engines/reputation-protection.md`

---

## PURPOSE

This module covers the full spectrum of executive-level communication — from board announcements and all-hands messages to investor updates, partnership announcements, crisis statements, and strategic vision declarations. Every communication type has its own architecture, audience, and risk profile.

---

## ALL-HANDS MESSAGE

The all-hands is the CEO's most important internal communication vehicle. It reaches the entire organization simultaneously and sets the tone for how people understand the company's direction, priorities, and leadership.

### Architecture
```
Opening: One sentence that names the reason for this message.
Context: What is happening (external or internal) that makes this message necessary.
The news or position: State it directly. Do not build to it.
What this means: For the company; for the teams; for individuals.
What is being done: Specific actions, specific owners, specific timelines.
What you need from them: One clear ask.
Close: A line that affirms confidence without being hollow.
```

### Tone: CEO/Founder profile (see `engines/tone-intelligence.md`)
- Direct; no hedge
- Human; not robotic corporate-speak
- Confident but not dismissive of concerns
- Action-oriented; not just explanatory

### Example — All-hands: major strategic shift
> This year's results showed us something we needed to see: the enterprise market is moving faster than our current product architecture can serve.
>
> That changes what we build this year. Instead of the three product lines we announced in January, we are consolidating to one — and it is the one our best customers have been asking us to build for 18 months.
>
> This is not a pivot driven by failure. This is a strategic choice to go deeper instead of wider while we still have the runway and team to do it right.
>
> What this means for each team is in the documents linked below. What I need from you is: read them, bring your questions to your manager by Friday, and trust that the decisions in there were not made lightly.
>
> Questions that are not answered in those documents come to me directly.

---

## BOARD ANNOUNCEMENT / UPDATE

Board communications require the highest precision and the lowest word count. Board members have seen hundreds of updates. They have no patience for narrative framing before the data.

### Architecture
```
Subject: [Specific topic — action or decision required vs. informational]
Situation: What is the current state. Data first.
Complication: What has changed or what requires attention.
Question: The specific question or decision this communication is about.
Answer / Recommendation: The recommended course of action.
Next steps: Who does what by when.
```

### Tone: Executive profile
- Conclusion first, evidence second
- Numbers are more credible than qualitative descriptions
- Confidence is demonstrated through preparation, not enthusiasm

### Example — Board update: financial performance
> Q3 Revenue: $4.2M (94% of plan; +28% YoY)
> Q3 Burn: $1.1M (8% under budget; driven by delayed engineering hires)
> Runway: 22 months at current burn
>
> Item requiring board input: The three senior engineering roles budgeted in Q3 are now available Q4. Filling them accelerates the enterprise product timeline by approximately 8 weeks. Total cost delta: +$310K against Q4 budget.
>
> Recommendation: Approve accelerated hiring. Details attached.
> Decision requested by: [date]

---

## INVESTOR UPDATE

Investor updates are trust infrastructure. Regular, honest communication with investors — especially through difficult periods — builds the relationship that supports the company through its hardest moments.

### Architecture
```
Quarter/Period: [X]
Headline: The one-sentence version of how things are going (honest)
Highlights: 3–5 specific achievements with numbers
Challenges: 2–3 honest descriptions of what is not working (with the plan to address)
Key metrics: The numbers that matter for this stage
Asks: What you need from investors right now
Next update: When they will hear from you again
```

### Tone: Executive profile — precise, credible, direct
Investor updates that only share good news lose credibility. The ones that acknowledge problems and show thoughtful response to them build the confidence that matters when things go wrong.

---

## CRISIS STATEMENT

A crisis statement has one job: reestablish trust in a situation where trust has been damaged. It does this through accountability, clarity, and demonstrated action — not through defensive explanation.

### Architecture
```
Acknowledgment: Name what happened, directly and specifically.
Accountability: Who is responsible (if the organization; own it fully).
Impact: What was the effect on affected parties (do not minimize).
Action: What has already been done.
Next steps: What will happen next, with specific timelines.
Commitment: One clear statement of what you commit to going forward.
```

### Tone: Crisis/Sensitive profile (see `engines/tone-intelligence.md`)
- No conditional apologies ("if anyone was affected...")
- No minimization ("what appeared to be an issue...")
- No passive accountability ("mistakes were made...")
- Shorter paragraphs than usual — easier to read under stress

### Example — Crisis: product failure affecting customers
> On [date], a system failure caused [specific impact] for [number] of our customers for approximately [time period].
>
> This was our failure. The cause was [specific technical or operational cause], which we should have caught in our review process. We did not.
>
> We have [specific action taken: refunded, restored, contacted, etc.]. Every affected account has been reached directly.
>
> The failure occurred because [root cause, briefly]. We have [specific fix] in place and are [specific preventive measure] to ensure it does not happen again. A full post-mortem will be published by [specific date].
>
> Our commitment: transparent communication when things go wrong. This falls short of what you deserve from us. We will demonstrate through action that it was not representative of how we operate.

---

## PARTNERSHIP ANNOUNCEMENT

Partnership announcements must communicate mutual value — what each party brings and what the combined result means for the audience.

### Architecture
```
What: The partnership (who + who)
Why: What each organization brings; why this combination
What it means: The specific outcome for customers, users, or the market
What's next: First concrete milestone or action
```

### Tone: Executive or CEO/Founder
- Focus on the outcome, not the process of reaching the agreement
- Avoid mutual praise that reads as backslapping
- Name one specific thing this enables that was not possible before

---

## PRODUCT LAUNCH MESSAGE

Leadership product launch communications are not marketing — they are strategic framing. The CEO's launch message sets the context for why this product exists, what problem it solves, and why now.

### Architecture
```
The problem: What exists in the world that this product addresses
The product: What it is and what it does (specific)
Why now: What made this the right moment
What it means: For the customer; for the market; for the company
How to access: The specific, frictionless next step
```

### Tone: CEO/Founder — brief, confident, product-first
Not: "We are thrilled to announce..."
Yes: "[Product name] launches today. Here is why it matters."

---

## DEPARTURE / RESIGNATION COMMUNICATION

### Executive announcing their own departure
- Lead with the positive (what is being moved toward)
- Acknowledge the organization with genuine specificity, not formula
- Keep it brief — no one needs a long farewell from an executive
- Do not settle scores, even obliquely

### Organization announcing an executive's departure
- If the departure is mutual and positive: brief acknowledgment, genuine thanks for specific contributions, smooth transition message
- If the departure is complicated: factual, brief, no speculation, transition information is the primary content
- If it is a termination: consult `engines/reputation-protection.md` and legal counsel before publishing

---

## STRATEGIC VISION DECLARATION

The annual or periodic public statement of where the organization is going.

### Architecture
```
Where we have been: A brief, honest acknowledgment of the prior period
Where we are: The honest current state (not a celebration, not a lament)
Where we are going: The vision — specific enough to be meaningful, broad enough to guide
Why: The external forces and internal conviction that drive this direction
How: The major strategic moves (2–3, not 10)
What we need: The capabilities, partnerships, or resources that will make it real
```

### Tone: CEO/Founder
- Declarative, not hedged
- Specific in direction, honest about uncertainty
- Shows that you have thought about this more than anyone else in the room

---

## RELATIONSHIP TO OTHER MODULES

- `engines/tone-intelligence.md` — CEO/Founder, Executive, Crisis profiles
- `engines/reputation-protection.md` — mandatory review for all crisis and sensitive communications
- `platforms/linkedin.md` — primary distribution platform for executive communications
- `core/quality-control.md` — scoring executive communications at threshold
