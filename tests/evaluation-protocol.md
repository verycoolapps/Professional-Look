# EVALUATION PROTOCOL
## Testing Methodology, Validation, and Improvement Cycle

**Module:** `tests/evaluation-protocol.md`
**Loaded by:** Quality assurance and version validation processes
**Dependencies:** `tests/test-cases.md`, `tests/quality-benchmarks.md`, `core/quality-control.md`

---

## PURPOSE

This module defines how PROFESSIONAL LOOK is systematically tested, validated, and improved. It covers pre-deployment validation, regression testing, user feedback integration, module isolation testing, integration testing, and the improvement cycle.

---

## PRE-DEPLOYMENT CHECKLIST

Before any version of this skill is deployed or distributed, verify:

### Architecture Verification
- [ ] All 32 files exist and are non-empty
- [ ] All internal file references use correct relative paths
- [ ] No file references a module that does not exist
- [ ] SKILL.md YAML frontmatter validates correctly
- [ ] Module routing table in SKILL.md is complete and accurate

### Content Verification
- [ ] Every file has substantive content (minimum 200 lines for most files)
- [ ] No file contains placeholder text ("TBD," "coming soon," "TODO")
- [ ] No conflicting instructions between modules (if two modules address the same topic, one defers to the other)
- [ ] Anti-slop engine's banned phrase dictionary does not itself contain banned phrases
- [ ] Quality control rubric dimensions sum to 100

### Progressive Disclosure Verification
- [ ] For each routing scenario in SKILL.md, verify every listed module exists
- [ ] Test five routing scenarios manually: LinkedIn post, CEO tone, crisis statement, content strategy, multilingual adaptation
- [ ] Verify that the correct modules load (and only those modules) for each scenario

### Cross-Reference Verification
- [ ] Every "see [module]" or "reference [module]" in any file points to a real module
- [ ] Dependency declarations at the top of each file match actual module relationships
- [ ] No circular dependencies (Module A requires Module B which requires Module A)

---

## FULL TEST SUITE PROTOCOL

### Step 1: Module Isolation Tests
Before integration testing, verify each module independently:

For each module, ask:
1. Does it load without errors?
2. Does it contain the required elements (Purpose, Scope, Activation, Workflow, Standards, Failure Modes, Examples, Dependencies)?
3. Is its content internally consistent?
4. Do its examples reflect the quality standards it describes?

### Step 2: Integration Tests (Selected from Test Cases)
Run at minimum these eight integration tests from `tests/test-cases.md`:

| Test | Rationale |
|---|---|
| TC-01: LinkedIn executive post | Tests writing engine + LinkedIn platform + executive tone |
| TC-02: AI slop cleanup | Tests anti-slop engine + rewriting engine |
| TC-03: CEO crisis statement | Tests crisis tone + executive communication + reputation protection |
| TC-07: Multilingual EN→ID | Tests multilingual module + rewriting engine |
| TC-12: Reputation risk review | Tests reputation protection module in isolation |
| TC-16: Content quality scoring | Tests quality control rubric accuracy |
| TC-25: Tone transformation | Tests tone engine + rewriting engine in combination |
| TC-30: Full ecosystem test | Tests maximum module activation and integration |

### Step 3: Full 30-Case Run
Run all 30 test cases from `tests/test-cases.md`.

Acceptance criteria: 28/30 pass (93.3%)
Disqualifiers: TC-03 (crisis statement) and TC-08 (data breach) must pass; failure on either is a blocker regardless of total score.

---

## REGRESSION TESTING PROTOCOL

When a module is modified, regression testing determines whether the change affected other modules.

### Regression Test Matrix

| Modified Module | Modules to Regression Test |
|---|---|
| SKILL.md | All routing scenarios; TC-30 |
| core/identity.md | TC-01, TC-05, TC-17, TC-30 |
| engines/anti-ai-slop-engine.md | TC-02, TC-04, TC-19, TC-25 |
| engines/tone-intelligence.md | TC-01, TC-03, TC-09, TC-25 |
| core/quality-control.md | TC-16, TC-26; recalibrate benchmarks |
| Any platform module | All test cases targeting that platform |
| intelligence/multilingual-communication.md | TC-07, TC-22 |
| engines/reputation-protection.md | TC-03, TC-08, TC-12, TC-27 |

### Regression pass criteria
All test cases in the regression matrix must pass. Any new failure introduced by a module change is a blocker.

---

## MODULE ISOLATION TESTING

Each module must be testable in isolation from others. Isolation test procedure:

**Step 1:** Load only the module being tested (plus core/identity.md as the universal base)
**Step 2:** Apply a task that would activate this module
**Step 3:** Verify the module delivers correct output within its defined scope
**Step 4:** Verify the module correctly flags its limitations (what it cannot do without other modules)

### Example — Isolating engines/anti-ai-slop-engine.md

Input: A sample text containing 8 known banned phrases
Expected behavior:
- All 8 phrases identified and flagged
- Correct substitution patterns provided for each
- No false positives on non-banned language

Pass: All 8 detected; 0 false positives; substitutions are appropriate

---

## EDGE CASE LIBRARY

These edge cases must be tested on every major version:

### EC-01: Blank Input
Input: No content, only a platform name
Expected: Ask for the content; do not generate without a brief

### EC-02: Ambiguous Task Class
Input: "Help me with this" + pasted text
Expected: Classify as REWRITE; proceed with appropriate mode selection

### EC-03: Conflicting Platform and Tone
Input: "Write a casual, emoji-heavy TikTok caption for a board-level compliance announcement"
Expected: Identify the conflict; offer two options; do not silently execute the problematic version

### EC-04: Undersized Input
Input: "Write a LinkedIn post" — no topic, no context
Expected: Request minimum viable brief; do not produce generic content

### EC-05: Reputation Red Flag
Input: Content with a clear defamation risk
Expected: Flag as RED; do not deliver the content as written; provide alternative

### EC-06: Perfect Input
Input: Content already scoring 90+ on the rubric
Expected: Deliver with minimal modification; do not over-edit; note that the content is strong

### EC-07: Below-Platform-Spec Length
Input: 2,000-word content for a tweet
Expected: Identify the length mismatch; offer to adapt to thread format or suggest a better platform

### EC-08: Request in Indonesian
Input: User writes the request in Indonesian
Expected: Respond in Indonesian; apply Indonesian professional register; treat as multilingual task

---

## FAILURE ANALYSIS TEMPLATE

When a test case fails, document using this template:

```
FAILURE REPORT

Test Case: [TC number and title]
Version: [Skill version being tested]
Date: [Date]
Tester: [Role or identifier]

EXPECTED BEHAVIOR:
[What should have happened]

ACTUAL BEHAVIOR:
[What actually happened]

DIMENSION FAILURES:
[List which scoring dimensions failed and by how much]

ROOT CAUSE:
[ ] Module not loading correctly
[ ] Module content is incorrect/incomplete
[ ] Module routing is wrong
[ ] Conflicting instructions between modules
[ ] Missing content in referenced module
[ ] Quality threshold not enforced
[ ] Anti-slop engine missed a pattern
[ ] Other: _______

AFFECTED MODULES:
[List the modules involved in the failure]

PROPOSED FIX:
[Specific change to be made]

REGRESSION RISK:
[Which other test cases might be affected by the fix]
```

---

## USER FEEDBACK INTEGRATION

When real-world users provide feedback on outputs:

### Positive Feedback
If users report that specific outputs were excellent:
1. Document the task type, modules activated, and output characteristics
2. Use as an additional benchmark example in `tests/quality-benchmarks.md`
3. Identify which module interactions produced the excellent result
4. Preserve those interactions in future versions

### Negative Feedback
If users report outputs that were below expectation:
1. Document the input, the output, and the specific complaint
2. Score the output against the quality rubric — was this a rubric failure or an expectation mismatch?
3. If rubric failure: identify which dimension failed and update the relevant module
4. If expectation mismatch: determine whether to update the skill's scope or communicate its scope more clearly

### Categorizing Feedback
| Feedback Type | Action |
|---|---|
| "Output had AI slop patterns" | Add phrase to anti-ai-slop-engine.md; update substitution patterns |
| "Tone was wrong for the context" | Review decision-engine.md tone selection logic |
| "Platform format was wrong" | Review reference/platform-formats.md specs |
| "Output was too generic / not specific enough" | Review writing-engine.md brief extraction; add specificity requirements |
| "Failed to flag a reputation risk" | Add risk category to reputation-protection.md |
| "Quality score was too low / too high" | Recalibrate quality-benchmarks.md; verify rubric application |
| "Modules loaded that weren't needed" | Review SKILL.md routing table |

---

## VERSION COMPARISON METHODOLOGY

When comparing a new version to a previous version:

**Step 1:** Run the full 30-case test suite on both versions
**Step 2:** For each test case, score both versions on all seven dimensions
**Step 3:** Calculate average dimension scores across all 30 cases
**Step 4:** Identify any test cases where the new version scores lower than the previous version
**Step 5:** Investigate any regressions before releasing the new version

### Acceptance criteria for a new version
- Average total score ≥ previous version average (no overall regression)
- No dimension average lower than previous version by more than 3 points
- No new failure on any of the eight mandatory integration tests
- All 30 edge cases produce appropriate behavior

---

## IMPROVEMENT CYCLE

```
USER FEEDBACK / TEST FAILURE
    ↓
ROOT CAUSE IDENTIFICATION
    ↓
MODULE TARGETED FOR UPDATE
    ↓
CHANGE DRAFTED
    ↓
MODULE ISOLATION TEST (verify fix works)
    ↓
REGRESSION TEST (verify fix doesn't break other tests)
    ↓
FULL TEST SUITE (verify overall quality maintained or improved)
    ↓
CHANGELOG UPDATED
    ↓
VERSION INCREMENTED
    ↓
DEPLOYMENT
```

---

## RELATIONSHIP TO OTHER MODULES

- `tests/test-cases.md` — the scenarios this protocol evaluates
- `tests/quality-benchmarks.md` — the scoring standards used in evaluation
- `core/quality-control.md` — the rubric applied in testing
- `CHANGELOG.md` — receives documented findings from each evaluation cycle
- All modules — each may be subject to modification based on evaluation findings
