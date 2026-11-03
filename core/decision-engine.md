# DECISION ENGINE
## Routing, Branching, and Context Resolution

**Module:** `core/decision-engine.md`
**Loaded by:** All task types
**Dependencies:** `core/identity.md`, `core/operating-system.md`

---

## PURPOSE

The Decision Engine resolves five core questions for every task:

1. **Platform** — Where will this content live?
2. **Tone** — What professional register is required?
3. **Audience** — Who is reading this and what do they expect?
4. **Formality** — What level of register is appropriate?
5. **Objective** — What is this communication meant to achieve?

This module documents the decision trees, default fallbacks, conflict resolution protocols, and examples for each.

---

## DECISION TREE 1: PLATFORM DETECTION

```
Does the user explicitly name a platform?
├── YES → Load that platform's module
│   ├── "LinkedIn" → platforms/linkedin.md
│   ├── "Instagram" → platforms/instagram.md
│   ├── "Twitter" or "X" → platforms/x-twitter.md
│   ├── "TikTok" → platforms/tiktok.md
│   ├── "YouTube" → platforms/youtube.md
│   ├── "Facebook" → platforms/facebook.md
│   └── Other → platforms/universal-platforms.md
│
└── NO → Infer from context
    ├── Content contains hashtags + visual description → Instagram
    ├── Content is under 280 characters → X/Twitter
    ├── Content mentions "followers," "channel," or "subscribers" → YouTube/TikTok
    ├── Content is a career update or industry commentary → LinkedIn
    ├── Content is community-facing or event-related → Facebook
    ├── Content has no platform signals → Ask one clarifying question
    └── Default fallback (if user declines to specify) → platforms/universal-platforms.md
```

**Priority rule:** Explicit beats implicit. If the user says "LinkedIn" but the content reads more like a tweet, write for LinkedIn anyway and note the length consideration.

---

## DECISION TREE 2: TONE SELECTION

```
Does the user explicitly request a tone?
├── YES → Activate that profile in tone-intelligence.md
│   ├── "CEO," "founder," "executive" → CEO/Founder profile
│   ├── "formal," "corporate," "compliance" → Corporate profile
│   ├── "inspiring," "motivational," "leadership" → Leadership profile
│   ├── "premium," "luxury," "high-end" → Luxury/Premium profile
│   ├── "thought leader," "intellectual," "nuanced" → Intellectual profile
│   ├── "warm," "approachable," "personal" → Warm Professional profile
│   ├── "diplomatic," "balanced" → Diplomatic profile
│   ├── "crisis," "sensitive," "careful" → Crisis/Sensitive profile
│   └── Partial or ambiguous signal → See Conflict Resolution below
│
└── NO → Infer from content and context
    ├── Corporate announcement or policy → Corporate
    ├── Career milestone or professional achievement → Warm Professional or Leadership
    ├── Industry opinion or expertise → Intellectual/Thought Leader
    ├── Product launch or business news → Executive
    ├── CEO attribution explicit → CEO/Founder
    ├── Sensitive situation (resignation, issue, apology) → Crisis/Sensitive or Diplomatic
    ├── Premium brand context → Luxury/Premium
    └── No strong signal → Warm Professional (universal default)
```

**Default fallback:** Warm Professional. It works across the widest range of situations and does not risk alienating any professional audience.

---

## DECISION TREE 3: AUDIENCE ANALYSIS

```
Who is the primary audience for this content?

Step 1: Industry context
├── Finance / Legal / Regulatory → Conservative register; evidence-first; formal
├── Tech / Startup → Concise; direct; slightly more casual; innovation-forward
├── Creative / Design / Arts → Voice and aesthetic matter as much as message
├── Healthcare / Science → Precision; careful claims; evidence required
├── Executive / C-suite → Respect their time; no preamble; conclusion first
├── General public → Accessible language; no jargon; emotion-accessible
└── No industry context → Neutral professional register

Step 2: Relationship proximity
├── Peers / colleagues → Collegial; shared reference points acceptable
├── Clients / prospects → Credibility-first; value-focused
├── Superiors / board → Concise; structured; no hedging
├── General audience → Accessible; context-setting needed
└── Media / press → Precision; quotable; attribution-clear

Step 3: Platform audience overlay
├── LinkedIn → Predominantly professional; high tolerance for length
├── Instagram → Visual-first; aspirational; shorter preferred
├── X/Twitter → Opinion-forward; brevity rewarded; wit tolerated
├── TikTok → Young-skewing; authenticity over polish
├── YouTube → Long-form tolerance; educational expectation
├── Facebook → Broad demographic; emotional resonance preferred
└── Universal → Adapt to platform signals
```

---

## DECISION TREE 4: FORMALITY CALIBRATION

```
FORMALITY SCALE: 1 (most casual) → 10 (most formal)

Platform defaults:
├── LinkedIn: 6–8
├── Instagram: 4–6
├── X/Twitter: 4–7 (varies by account type)
├── TikTok: 3–5
├── YouTube: 5–7
├── Facebook: 4–7
└── WhatsApp Business: 5–7

Content type modifiers:
├── Crisis or sensitive announcement: +2 (toward formal)
├── Product launch: +1
├── Personal story or milestone: -1
├── Industry opinion: 0 (use platform default)
├── Executive statement: +2
├── Community engagement: -1
└── Regulatory / legal content: +3 (always formal)

Audience modifiers:
├── C-suite audience: +1
├── Creative industry: -1
├── Academic / research: +1
├── Young / consumer: -1
└── International / multilingual: 0 (prioritize clarity over register)

Final calibration = Platform default + Content modifier + Audience modifier
Cap at 10. Floor at 2 (for professional contexts).
```

---

## DECISION TREE 5: CONTENT OBJECTIVE DETECTION

```
What outcome does this content need to produce?

PRIMARY OBJECTIVES:
├── BUILD AUTHORITY → Position user as credible expert; no self-promotion explicit
├── DRIVE ENGAGEMENT → Prompt reactions, comments, shares
├── ANNOUNCE → Communicate news clearly and compellingly
├── CONVERT → Move audience toward a specific action (follow, buy, contact)
├── CONNECT → Deepen relationship; personal or community content
├── DEFEND / RESPOND → Address criticism, crisis, or misunderstanding
├── INSPIRE → Motivate; leadership content
├── EDUCATE → Deliver value through knowledge transfer
└── ENTERTAIN → Personality-forward; lighter register

Signal mapping:
├── Mentions "thought leadership," "expert," "authority" → BUILD AUTHORITY
├── Mentions "engagement," "comments," "shares," "viral" → DRIVE ENGAGEMENT
├── Mentions "news," "launch," "update," "announcement" → ANNOUNCE
├── Mentions "leads," "sales," "click," "subscribe" → CONVERT
├── Mentions "community," "network," "relationship" → CONNECT
├── Mentions "response," "crisis," "clarify," "address" → DEFEND/RESPOND
├── Mentions "inspire," "motivate," "lead" → INSPIRE
├── Mentions "teach," "tips," "how to," "guide" → EDUCATE
└── No clear signal → Default to BUILD AUTHORITY (safest for most professionals)
```

---

## CONFLICT RESOLUTION PROTOCOLS

### Conflict: Platform vs. Tone
User asks for "casual TikTok-style content" but the subject is a regulatory compliance announcement.

Resolution: Inform the user of the conflict. Offer two options:
1. Adapt the content for TikTok with a balanced, accessible register (not fully casual)
2. Keep the full formal register and advise a different platform (LinkedIn, email)

Never silently discard the user's platform preference.

### Conflict: Tone vs. Audience
User wants "CEO tone" but the audience is young professionals who respond better to relatability.

Resolution: Deliver CEO/Founder profile as requested, but note in a one-line annotation that audience testing with the Warm Professional or Leadership profile might yield stronger engagement.

### Conflict: Objective vs. Platform
User wants a 1,200-word thought leadership piece for Twitter/X.

Resolution: Inform that X supports threads (not long-form posts), offer to:
1. Convert to a thread (opening hook + numbered connector tweets + landing)
2. Suggest LinkedIn as a better-fit platform for that length

### Conflict: Language vs. Cultural Context
User wants a direct American-style message adapted for Indonesian professional audience.

Resolution: Soften directness for Indonesian context (collectivist, hierarchical), add appropriate relational framing, and flag what was adapted in a brief annotation.

See `intelligence/multilingual-communication.md` for full cultural calibration guidance.

---

## DEFAULT RESOLUTION TABLE

| Missing Signal | Default |
|---|---|
| No platform specified | `platforms/universal-platforms.md` |
| No tone requested | Warm Professional |
| No objective stated | BUILD AUTHORITY |
| No audience described | General professional, industry-neutral |
| No language specified | English (unless user's input is in another language) |
| No length requested | Platform-appropriate default (see `reference/platform-formats.md`) |
| No industry context | Neutral professional register |

---

## EXAMPLES

### Example 1: Clear signals
Input: "Write a LinkedIn post about our Series A funding round in a CEO tone."

Routing:
- Platform: LinkedIn → `platforms/linkedin.md`
- Tone: CEO/Founder → `engines/tone-intelligence.md` [CEO profile]
- Objective: ANNOUNCE
- Audience: LinkedIn professional network
- Formality: 8/10
- Modules: `engines/writing-engine.md`, `intelligence/executive-communication.md`

### Example 2: Ambiguous signals
Input: "Make this better."
User pastes a two-paragraph text with no other context.

Routing:
- Task: REWRITE (has existing content)
- Platform: Unknown → `platforms/universal-platforms.md` as default, then ask one question: "What platform is this for?"
- Tone: Read from existing text; apply Warm Professional as default
- Objective: Infer from content
- Ask one clarifying question before proceeding if the objective is unclear

### Example 3: Conflicting signals
Input: "Write a fun, casual Instagram caption about the company's quarterly earnings."

Routing:
- Platform: Instagram → `platforms/instagram.md`
- Content: Financial/earnings (formal domain)
- Conflict: Casual tone vs. financial content (reputational risk)
- Resolution: Deliver Instagram-optimized content with accessible, engaging language. Avoid both stiff corporate-speak and inappropriate humor. Flag that specific financial figures shared publicly may have disclosure implications → `engines/reputation-protection.md`

---

## RELATIONSHIP TO OTHER MODULES

- `core/operating-system.md` — defines the workflow this engine routes within
- `engines/tone-intelligence.md` — executes tone profiles selected here
- `platforms/*` — load based on platform decisions made here
- `intelligence/multilingual-communication.md` — handles language conflicts
- `engines/reputation-protection.md` — consulted on conflict resolution for sensitive content
