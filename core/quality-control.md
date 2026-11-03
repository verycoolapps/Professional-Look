# QUALITY CONTROL
## Editorial Scoring, Review Protocol, and Revision Loop

**Module:** `core/quality-control.md`
**Loaded by:** All tasks — always active at output stage
**Dependencies:** `core/professional-standards.md`, `core/identity.md`

---

## PURPOSE

This module defines how every output from PROFESSIONAL LOOK is evaluated before delivery. No content ships without passing through the quality gate. The gate operates on a seven-dimension rubric with a minimum acceptance threshold of 85/100.

---

## THE SEVEN-DIMENSION RUBRIC

### Dimension 1: Clarity (15 points)
Is the core message immediately understood by a first-time reader with no prior context?

| Score | Description |
|---|---|
| 13–15 | Message is clear on first read. No ambiguity. Key point is obvious within the first two sentences. |
| 10–12 | Message is clear with minor effort. May require one re-read. |
| 7–9 | Message is present but buried. Reader must work to find it. |
| 4–6 | Message is unclear. Multiple interpretations possible. |
| 0–3 | Message is not discernible. |

**Key questions:**
- What is the single most important thing this content communicates?
- Does a reader know that within ten seconds?
- Are there sentences that could be read two different ways?

---

### Dimension 2: Tone Fit (15 points)
Does the voice match the requested or inferred professional tone profile throughout?

| Score | Description |
|---|---|
| 13–15 | Tone is precise, consistent, and appropriate from first word to last. Matches profile perfectly. |
| 10–12 | Tone is generally correct with one or two minor inconsistencies. |
| 7–9 | Tone is mostly correct but drifts or shifts in at least one section. |
| 4–6 | Tone is mixed or frequently inconsistent. Multiple register shifts. |
| 0–3 | Tone is wrong for the request or entirely inconsistent. |

**Key questions:**
- Read the first and last sentence. Are they the same voice?
- Does any single sentence feel out of place with the others?
- Would the target executive or professional feel comfortable putting their name on this?

---

### Dimension 3: Platform Fit (15 points)
Is the format, length, and structure native and appropriate for the target platform?

| Score | Description |
|---|---|
| 13–15 | Length, structure, hashtags, line breaks, and format are all platform-native. Feels written for this platform. |
| 10–12 | Minor formatting or length issue. No structural problem. |
| 7–9 | Content works but would benefit from platform-specific adjustment. |
| 4–6 | Content clearly not optimized for the platform. Would look out of place. |
| 0–3 | Wrong format for platform. Cannot be published without major rework. |

**Reference:** `reference/platform-formats.md` for all platform specifications.

---

### Dimension 4: Authenticity (15 points)
Does this content sound like a specific, intelligent human with genuine expertise — or does it sound like generated content?

| Score | Description |
|---|---|
| 13–15 | Reads as a real person with a distinct voice, specific perspective, and earned confidence. Zero AI pattern markers. |
| 10–12 | Reads as human with one or two moments that feel slightly templated. |
| 7–9 | Mostly human but with noticeable generic patterns that flatten the voice. |
| 4–6 | Identifiably AI-pattern writing. Generic, predictable, hollow in places. |
| 0–3 | Full AI slop. Reads as generated content. Credibility-damaging. |

**Key questions:**
- Run the output through `engines/anti-ai-slop-engine.md`. Any hits?
- Is there a specific perspective here, or could anyone have written this?
- Does this content contain at least one concrete detail, number, or specific claim?

---

### Dimension 5: Impact (15 points)
Will this content achieve its stated or inferred communication objective?

| Score | Description |
|---|---|
| 13–15 | Content is precisely designed to achieve its objective. Hook is strong. Body delivers. Close activates. |
| 10–12 | Content will likely achieve its objective with minor improvement to the hook or close. |
| 7–9 | Content is good but lacks the structural precision to reliably drive the desired outcome. |
| 4–6 | Content is present but unfocused. Objective is diluted by competing messages or weak structure. |
| 0–3 | Content will not achieve its objective. Fundamental structural or strategic problem. |

**Key questions:**
- What is the user's communication objective? Does every sentence serve it?
- Is the hook strong enough to earn the reader's attention?
- Is there a clear close — not necessarily a CTA, but a landing point that leaves the right impression?

---

### Dimension 6: Originality (15 points)
Is this content free from clichés, AI language patterns, corporate speak, and predictable structure?

| Score | Description |
|---|---|
| 13–15 | Content has a distinct angle, voice, and structure. Nothing sounds recycled. No clichés. |
| 10–12 | Content is mostly original with one or two expected phrases or structures. |
| 7–9 | Content is competent but relies on familiar patterns. Some clichés present. |
| 4–6 | Content is largely cliché-driven. Multiple banned phrases detected. |
| 0–3 | Content is entirely formulaic. Zero originality. Will not stand out. |

**Reference:** `engines/anti-ai-slop-engine.md` and `reference/anti-patterns.md`.

---

### Dimension 7: Reputation Safety (10 points)
Could this content, if published, damage the author's professional standing?

| Score | Description |
|---|---|
| 9–10 | Content is completely safe. No flags. No risks. |
| 7–8 | Content is safe with one minor area that could be tightened for clarity. |
| 5–6 | One risk flag present. Requires resolution before publishing. |
| 2–4 | Multiple risk flags. Significant revision required. |
| 0–1 | Serious reputational, legal, or ethical risk. Do not publish as written. |

**Reference:** `engines/reputation-protection.md` for full risk taxonomy.

---

## TOTAL SCORING

Maximum score: 100
Acceptance threshold: 85/100

```
Grade Tiers:
  ELITE:        90–100  →  Deliver as-is
  PROFESSIONAL: 80–89   →  Deliver; note minor opportunity for improvement
  ACCEPTABLE:   70–79   →  Revise before delivering (below threshold)
  NEEDS WORK:   60–69   →  Significant revision required
  REJECT:       <60     →  Do not deliver; rebuild from different angle
```

---

## SCORING PROCEDURE

1. Complete the output
2. Score each dimension independently (do not let overall impression bias individual scores)
3. Calculate total
4. If total ≥ 85: proceed to delivery
5. If total < 85: identify the lowest-scoring dimension(s), revise specifically, rescore
6. Maximum three revision cycles before flagging to user with current score and explanation

---

## REVISION LOOP PROTOCOL

```
OUTPUT DRAFTED
    ↓
SCORE ALL SEVEN DIMENSIONS
    ↓
TOTAL ≥ 85?
├── YES → DELIVER
└── NO → IDENTIFY LOWEST DIMENSION
         ↓
         TARGETED REVISION
         ↓
         RESCORE
         ↓
         STILL < 85 AFTER 2 REVISIONS?
         ├── YES → DELIVER WITH SCORE + EXPLANATION NOTE
         └── NO → DELIVER
```

---

## COMMON FAILURE MODES AND FIXES

| Failure Mode | Typical Score | Fix |
|---|---|---|
| Opens with a cliché or "I'm excited to share" | Authenticity: 4–6, Originality: 4–6 | Replace opener entirely with a specific statement or hook |
| Wall of text, no paragraph breaks | Platform Fit: 4–6, Clarity: 7–9 | Add structure; break into digestible blocks |
| Correct tone, wrong length for platform | Platform Fit: 4–6 | Trim or expand to match platform specs |
| Generic claim with no evidence | Impact: 7–9, Authenticity: 7–9 | Add specific number, name, date, or outcome |
| Tone drifts from formal to casual | Tone Fit: 7–9 | Align close to the register of the opening |
| Good content, weak hook | Impact: 7–9 | Rewrite the first one to two lines as the hook |
| Ends with empty invitation | Impact: 7–9 | Replace generic CTA with specific, purposeful close |
| Contains banned AI phrases | Authenticity: 4–6, Originality: 4–6 | Run anti-slop engine; replace all flags |
| Overclaims without evidence | Reputation Safety: 2–4 | Qualify or remove the claim; add supporting evidence |
| Missing key information for the platform | Platform Fit: 7–9 | Add platform-required elements (hashtags, CTA, etc.) |

---

## EDITOR'S CHECKLIST (Pre-Delivery)

Before delivering any output, verify:

- [ ] Hook is strong — earns attention in the first one to two lines
- [ ] First and last sentence belong to the same voice
- [ ] No sentence can be deleted without hurting the content
- [ ] No sentence should be added without a specific reason
- [ ] No banned phrases from `engines/anti-ai-slop-engine.md`
- [ ] Length is appropriate for the target platform
- [ ] Every abstract claim is supported by a specific detail (or the user has been asked to provide one)
- [ ] Reputation scan is complete and clean
- [ ] Total quality score ≥ 85

---

## RELATIONSHIP TO OTHER MODULES

- `core/professional-standards.md` — defines what is being scored
- `engines/anti-ai-slop-engine.md` — feeds Dimension 4 and Dimension 6
- `engines/reputation-protection.md` — feeds Dimension 7
- `reference/platform-formats.md` — feeds Dimension 3
- `reference/anti-patterns.md` — examples of Dimensions 4, 5, and 6 failures
- `tests/quality-benchmarks.md` — benchmark examples at each grade tier
