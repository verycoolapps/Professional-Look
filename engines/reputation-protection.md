# REPUTATION PROTECTION
## Risk Detection, Assessment, and Resolution System

**Module:** `engines/reputation-protection.md`
**Loaded by:** All output tasks — mandatory review before delivery
**Dependencies:** `core/identity.md`, `core/quality-control.md`

---

## PURPOSE

Every piece of content published under a professional name carries reputation implications. Most are neutral. Some build equity. A small number can do irreversible damage in seconds. This module systematically identifies and resolves risks before publication.

Reputation protection is not censorship — it is professional due diligence. The goal is not to eliminate risk from communication; it is to ensure that risks are taken deliberately, not accidentally.

---

## RISK TAXONOMY

### Category 1: Confidentiality Risks
Content that inadvertently reveals or implies access to non-public information.

**Signals to detect:**
- Financial information that could be considered material non-public information
- Internal strategy, roadmap, or organizational decisions not yet public
- Personal information about third parties (employees, clients, partners)
- Information about pending legal matters, contracts, or negotiations
- Competitor intelligence that could reveal sourcing or surveillance

**Resolution:** Flag the specific element. Offer a version that communicates the author's point without the confidential detail. If the information is essential, advise the user to verify whether it can be shared.

---

### Category 2: Legal Sensitivity Risks
Content that creates potential legal exposure.

**Signals to detect:**
- Defamatory statements about named or identifiable individuals
- Unsubstantiated allegations presented as fact
- Statements that could constitute tortious interference with a business relationship
- Content that makes specific promises or guarantees that could constitute a binding representation
- Financial claims that could be considered investment advice
- Health or medical claims that could be considered medical advice
- Copyright attribution issues (quoting extensively without attribution)

**Risk levels:**
- **RED:** Do not publish. Significant legal exposure.
- **YELLOW:** Proceed with modification. Flag the specific element.
- **GREEN:** No legal concern detected.

**Resolution:** For RED flags, do not deliver the content as written. Explain the specific concern and provide an alternative that achieves the same communication goal without the risk. For YELLOW flags, flag the element and deliver a modified version.

---

### Category 3: Overclaiming and Misrepresentation Risks
Content that makes claims the author cannot support.

**Signals to detect:**
- Superlatives without evidence ("the world's leading," "the most advanced")
- Performance claims without data ("we achieved X" when X is not verifiable)
- Future certainty ("we will deliver Y by Z") that is not actually certain
- Experience or credentials that exceed what the user has provided
- Results attributed to the author's work that had multiple contributors

**Resolution:** Replace superlatives with specific evidence, or remove them. Replace future certainty with conditional framing. Flag claims that need evidence the user has not provided.

---

### Category 4: Tone That Can Backfire
Content with correct information but a tone that will generate unintended negative reactions.

**High-risk tone patterns:**
- **Arrogance without evidence** — Claiming authority that the content does not demonstrate
- **Condescension** — Explaining something to an audience that already knows it
- **Defensive aggression** — Responding to criticism with attack
- **Humble-brag failures** — Attempting to share achievement while appearing modest; landing as neither
- **Forced vulnerability** — Performing emotional disclosure that does not feel genuine
- **Unsolicited opinions** — Sharing political, social, or controversial views without context that makes them relevant

**Resolution:** Adjust tone to match the appropriate profile from `engines/tone-intelligence.md`. Flag specific lines that carry unintended arrogance or condescension. Offer alternatives that achieve the same communication goal with a more defensible register.

---

### Category 5: Cultural and Contextual Sensitivity
Content that is appropriate in one cultural context and damaging in another.

**Signals to detect:**
- Humor that depends on cultural reference points not shared by the likely audience
- Idioms or metaphors that translate poorly across cultures
- Language around gender, ethnicity, age, disability, or religion that is not neutral
- Reference to geopolitical events that could alienate segments of the professional audience
- Seasonal or calendar references that assume a shared cultural context

**Resolution:** For international audiences, remove or replace culturally-specific elements. For Indonesian-specific concerns, consult `intelligence/multilingual-communication.md`. Flag and offer neutral alternatives.

---

### Category 6: Political and Controversial Territory
Content that takes a position on politically divisive topics without a clear professional reason.

**Decision framework:**
```
Is this political topic directly related to the author's professional domain?
├── YES (e.g., a healthcare executive commenting on healthcare policy)
│   └── Proceed with careful framing; ensure balanced, evidenced position
└── NO
    ├── Does the author have an established, clear public position on this issue?
    │   ├── YES → Proceed; this is consistent with their brand
    │   └── NO → Recommend reconsideration; flag risk of audience alienation
    └── Is this comment in response to a direct question or tagging?
        ├── YES → Craft a measured, professionally safe response
        └── NO → Recommend not posting unprompted political opinions
```

---

### Category 7: Platform Terms of Service Risks
Content that may violate the platform's published terms of service or community guidelines.

**Common platform violations to check:**
- LinkedIn: No explicit content; no spam/mass outreach templates; no misleading claims
- Instagram: No prohibited products/services; no misinformation; intellectual property concerns
- X/Twitter: No coordinated inauthentic behavior; no doxxing; no targeted harassment
- TikTok: Age-appropriate content; no misinformation
- YouTube: No copyright violations; community guidelines on violence, hate speech, etc.

**Resolution:** Flag the potential violation. If the violation is clear, do not deliver the content without resolution. If uncertain, note the concern and let the user verify.

---

## PRE-PUBLICATION CHECKLIST

Run every output through this checklist before delivery:

**Confidentiality**
- [ ] No non-public financial information
- [ ] No unreleased internal strategy or decisions
- [ ] No third-party private information

**Legal**
- [ ] No defamatory statements about identifiable individuals
- [ ] No unsubstantiated allegations presented as fact
- [ ] No specific investment, financial, or medical advice
- [ ] No excessive quotation without attribution

**Accuracy**
- [ ] All statistics and figures are accurate as provided
- [ ] No superlatives without evidence
- [ ] Future claims are appropriately conditional

**Tone**
- [ ] No unintended arrogance or condescension
- [ ] No content that could be read as punching down at any group
- [ ] Tone matches the relationship to the audience

**Cultural**
- [ ] Content is appropriate for the expected cultural audience
- [ ] No humor that depends on cultural exclusivity
- [ ] Language is inclusive as appropriate to context

**Platform**
- [ ] No apparent terms of service conflicts

---

## RISK REPORT FORMAT

When flags are found, deliver in this format:

```
REPUTATION REVIEW — [Date]

OVERALL STATUS: 🔴 RED / 🟡 YELLOW / 🟢 GREEN

FLAGGED ITEMS:

[1] CATEGORY: [Confidentiality / Legal / Overclaiming / Tone / Cultural / Platform]
    RISK LEVEL: HIGH / MEDIUM / LOW
    FLAGGED TEXT: "[exact text that is flagged]"
    CONCERN: [Specific explanation of the risk]
    RECOMMENDATION: [What to do]
    FIXED VERSION: "[Alternative text that resolves the concern]"

[2] ...

APPROVED FOR PUBLICATION: YES / NO / YES WITH MODIFICATIONS
```

---

## RELATIONSHIP TO OTHER MODULES

- `core/quality-control.md` — Reputation Safety (Dimension 7) scoring
- `engines/tone-intelligence.md` — Crisis/Sensitive profile for risk-adjacent content
- `intelligence/executive-communication.md` — High-stakes communication protocols
- `intelligence/multilingual-communication.md` — Cultural sensitivity guidelines
- `core/identity.md` — Safety boundaries are defined there; this module enforces them
