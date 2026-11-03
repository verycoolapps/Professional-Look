# TEST CASES
## 30 Realistic Scenarios for PROFESSIONAL LOOK Validation

**Module:** `tests/test-cases.md`
**Loaded by:** Testing and validation procedures
**Dependencies:** All modules

---

## PURPOSE

These 30 test scenarios cover the full operational range of PROFESSIONAL LOOK. Each case includes the input, platform, tone, expected module activation, expected output characteristics, and pass/fail criteria. Testing a new version requires all 30 cases to pass.

---

## TEST CASE 1: LinkedIn Executive Post — Product Launch

**Input:** "Write a LinkedIn post about our new HR software for small businesses. It helps with payroll and compliance."
**Platform:** LinkedIn
**Tone:** Executive
**Modules expected:** writing-engine, tone-intelligence [Executive], platforms/linkedin, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Opens with a specific problem or context, not "Excited to announce..."
- Names the software with a specific capability
- 150–300 words
- Clean paragraph structure
- Ends with a specific next step or question
**Pass criteria:** Score ≥ 85; no banned phrases; platform-native format

---

## TEST CASE 2: Rewrite — AI Slop Cleanup

**Input:** "In today's fast-paced business environment, it's crucial to leverage synergies and unlock your team's full potential. By embracing innovative strategies and moving the needle on core metrics, we can create game-changing paradigm shifts."
**Task:** Rewrite — Deep Edit
**Platform:** LinkedIn
**Tone:** Executive
**Modules expected:** rewriting-engine, anti-ai-slop-engine, tone-intelligence, quality-control
**Expected output characteristics:**
- Zero banned phrases from anti-ai-slop-engine
- Specific content replacing the abstract original
- Request for specific details if content is too thin to fill with substance
**Pass criteria:** Score ≥ 85; all flagged phrases replaced; content now carries actual meaning

---

## TEST CASE 3: CEO-Level All-Hands Message

**Input:** "Write an all-hands message. We're pivoting from SMB to enterprise. Layoffs affected 12% of the team."
**Platform:** Internal communication (email/Slack)
**Tone:** CEO/Founder
**Modules expected:** tone-intelligence [CEO/Founder], intelligence/executive-communication, reputation-protection, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Leads with the reality, not a preamble
- Acknowledges affected employees specifically
- States the reason without spin
- Provides specific next steps
- No passive voice on accountability
**Pass criteria:** Score ≥ 88 (elevated threshold for sensitive communication); no conditional apologies; no passive accountability constructions

---

## TEST CASE 4: Instagram Caption — Personal Brand

**Input:** "Caption for a photo of me speaking at a conference. I'm a leadership coach. The conference was for mid-level managers."
**Platform:** Instagram
**Tone:** Warm Professional
**Modules expected:** writing-engine, tone-intelligence [Warm Professional], platforms/instagram, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Hook in first line (before "more" truncation)
- 80–150 words total
- Ends with specific question or invitation
- No "Honored and grateful to be here!" opener
- Hashtags at end (3–5 relevant tags)
**Pass criteria:** Score ≥ 85; hook earns the read; Instagram-native format

---

## TEST CASE 5: X/Twitter Thread — Industry Insight

**Input:** "Write a thread about why most product managers focus on the wrong metrics. I think retention is always more important than acquisition."
**Platform:** X/Twitter
**Tone:** Intellectual/Thought Leader
**Modules expected:** writing-engine, tone-intelligence [Intellectual], platforms/x-twitter, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Hook tweet makes the claim directly (5–7 tweets total)
- Each tweet stands alone
- Evidence and mechanism in body tweets
- Landing tweet delivers the synthesis
- Under 280 characters per tweet
**Pass criteria:** Score ≥ 85; no tweet exceeds 280 characters; position is clear and defended

---

## TEST CASE 6: Personal Brand Strategy — New Audience

**Input:** "I'm a CFO who wants to build a personal brand on LinkedIn. I've been in finance for 20 years. I want to be known as someone who makes complex financial strategy understandable."
**Task:** Strategize
**Platform:** LinkedIn
**Tone:** Intellectual/Thought Leader
**Modules expected:** intelligence/personal-branding, intelligence/content-strategy, intelligence/audience-psychology, platforms/linkedin, recommendation-engine, quality-control
**Expected output characteristics:**
- Positioning statement
- 3–5 content pillars with specific topic suggestions
- Content archetypes and ratio recommendation
- Posting frequency guidance
- First three post ideas with hooks
**Pass criteria:** Positioning is specific and ownable; pillars are differentiated; topic suggestions are specific, not generic

---

## TEST CASE 7: Multilingual Adaptation — EN to ID

**Input:** "Translate and adapt this LinkedIn post for an Indonesian professional audience: 'The best CEOs I've worked with share one trait: they're comfortable saying what they don't know. Confidence isn't certainty. It's the ability to make decisions under uncertainty and own the outcomes.'"
**Platform:** LinkedIn
**Language:** Indonesian (professional Bahasa)
**Modules expected:** intelligence/multilingual-communication, engines/rewriting-engine, platforms/linkedin, quality-control
**Expected output characteristics:**
- Translated with meaning-first approach (not word-for-word)
- Register: modern professional Bahasa
- Cultural adaptation: appropriate modesty framing, appropriate relational register
- Maintains the core insight
**Pass criteria:** Reads naturally to an Indonesian professional; no awkward literal translations; culturally appropriate

---

## TEST CASE 8: Crisis Statement — Public Service Failure

**Input:** "Our app had a data breach. 50,000 users' email addresses were exposed for 6 hours before we caught it. We need to post a statement."
**Platform:** LinkedIn + Company Website
**Tone:** Crisis/Sensitive
**Modules expected:** tone-intelligence [Crisis/Sensitive], intelligence/executive-communication, reputation-protection, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Leads with what happened (specific: "50,000 users' email addresses")
- No conditional language ("may have been affected")
- States specific duration ("6 hours")
- Names specific actions taken and next steps
- No corporate-speak minimization
**Pass criteria:** Score ≥ 90 (critical); full accountability language; no minimization; specific facts

---

## TEST CASE 9: TikTok Hook and Script — Educational

**Input:** "Script a 60-second TikTok about the difference between a manager and a leader. I'm an executive coach."
**Platform:** TikTok
**Tone:** Warm Professional
**Modules expected:** writing-engine, tone-intelligence [Warm Professional], platforms/tiktok, quality-control
**Expected output characteristics:**
- Hook script for 0–3 seconds
- Full 60-second script with timing markers
- On-screen text suggestions
- Conversational, spoken language (not written language)
- CTA at end
**Pass criteria:** Hook would stop a scroll; script is 60 seconds at natural speech pace; language sounds spoken, not written

---

## TEST CASE 10: YouTube Title — Counterintuitive Content

**Input:** "I made a video about why I think most LinkedIn advice makes people worse at their careers. What should I title it?"
**Platform:** YouTube
**Task:** Title only
**Modules expected:** platforms/youtube, writing-engine, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- 3 title options
- Each under 65 characters
- Each creates curiosity without clickbait
- Primary keyword included naturally
- Counter-narrative framing where appropriate
**Pass criteria:** All three titles would earn a click from the intended audience; none overpromise; all are under 65 characters

---

## TEST CASE 11: LinkedIn Bio Optimization

**Input:** "Current headline: 'Senior Marketing Manager at [Company]'. Please optimize."
**Platform:** LinkedIn profile
**Task:** Rewrite — Structural Overhaul for profile element
**Modules expected:** rewriting-engine, platforms/linkedin, intelligence/personal-branding, quality-control
**Expected output characteristics:**
- New headline under 220 characters
- Value proposition format (what you do → for whom → differentiator)
- Not just a job title
**Pass criteria:** Headline includes specific value proposition; no filler; under 220 characters

---

## TEST CASE 12: Reputation Risk Review

**Input:** "About to post this. Let me know if there are any risks: 'Just heard that [Competitor Company] lost their biggest client. When companies prioritize valuation over value, this is what happens. Happy to take calls from their team.'"
**Task:** Protect
**Platform:** LinkedIn
**Modules expected:** reputation-protection, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Risk report with specific flags
- RED/YELLOW/GREEN status
- Specific flagged phrases
- Fixed alternatives for each flag
**Pass criteria:** All risks identified; at minimum: reputation risk for competitor disparagement, professional tone concern, potential backlash

---

## TEST CASE 13: Facebook Organizational Announcement

**Input:** "Write a Facebook post announcing that our nonprofit is opening a new community center in [City]. Opening is in 3 months."
**Platform:** Facebook
**Tone:** Leadership (warm, community-focused)
**Modules expected:** writing-engine, tone-intelligence [Leadership], platforms/facebook, quality-control
**Expected output characteristics:**
- Community-first framing (what this means for the community, not the organization)
- Specific date placeholder
- Clear next step (how to get involved or learn more)
- 100–200 words
**Pass criteria:** Warm tone; community benefit clear; specific date/details present or flagged for input

---

## TEST CASE 14: WhatsApp Business Broadcast

**Input:** "Write a WhatsApp broadcast to our existing customers about a 20% anniversary sale. We've been in business 5 years."
**Platform:** WhatsApp Business
**Tone:** Warm Professional
**Modules expected:** writing-engine, tone-intelligence [Warm Professional], platforms/universal-platforms, quality-control
**Expected output characteristics:**
- Under 100 words
- Conversational register (not corporate)
- Clear offer and how to access it
- No marketing speak
**Pass criteria:** Reads as a message from a person, not a blast; offer and CTA clear; under 100 words

---

## TEST CASE 15: Medium Article Opening

**Input:** "Write the opening 3 paragraphs for an article about why employee surveys don't work. I'm an HR director with 15 years of experience."
**Platform:** Medium
**Tone:** Intellectual/Thought Leader
**Modules expected:** writing-engine, tone-intelligence [Intellectual], platforms/universal-platforms, engines/anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Opens with a specific, credible claim (not "employee surveys are broken")
- Establishes author's authority through specific experience
- Creates a "read more" pull by the end of paragraph 3
- No hollow openers
**Pass criteria:** First paragraph earns the read; authority established through specificity, not credential listing

---

## TEST CASE 16: Thread Quality Check — LinkedIn

**Input:** User pastes a 500-word LinkedIn post. "Score this and tell me what to fix."
**Task:** Analyze
**Modules expected:** quality-control, anti-ai-slop-engine, platforms/linkedin, recommendation-engine
**Expected output characteristics:**
- Dimension-by-dimension scores
- Top 3 specific issues
- Specific fix for each
- Total score
**Pass criteria:** Scoring is accurate; fixes are specific (not "improve the hook" but "the first line states context; replace with the finding in paragraph 3"); score matches subjective quality

---

## TEST CASE 17: CEO Announcement — Partnership

**Input:** "Write a LinkedIn post from our CEO announcing a strategic partnership with [Major Company]."
**Platform:** LinkedIn
**Tone:** CEO/Founder
**Modules expected:** writing-engine, tone-intelligence [CEO/Founder], intelligence/executive-communication, platforms/linkedin, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Announces the partnership without "thrilled/honored/excited to"
- Names what this partnership enables that was not possible before
- CEO-level brevity (under 250 words)
**Pass criteria:** No hollow enthusiasm; specific value proposition of the partnership stated; CEO/Founder tone consistent throughout

---

## TEST CASE 18: Content Strategy for New Creator

**Input:** "I'm a data scientist who wants to build an audience on LinkedIn. I have no posts yet. What should I do?"
**Task:** Strategize
**Platform:** LinkedIn (primary)
**Modules expected:** intelligence/personal-branding, intelligence/content-strategy, intelligence/audience-psychology, recommendation-engine
**Expected output characteristics:**
- Positioning guidance
- 3 content pillars specific to data science professionals
- First month content plan (8–12 topics)
- How to get early traction without existing following
**Pass criteria:** Pillars are specific to data science (not generic "expertise, human, educational"); topics have actual hooks; month one plan is actionable from day one

---

## TEST CASE 19: Instagram Carousel Copy

**Input:** "I'm making a carousel about the 5 most common salary negotiation mistakes. Write copy for each slide."
**Platform:** Instagram
**Tone:** Warm Professional
**Task:** Create
**Modules expected:** writing-engine, tone-intelligence [Warm Professional], platforms/instagram, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Slide 1: Hook slide (promise)
- Slides 2–6: One mistake per slide with headline + 1–2 sentence explanation
- Slide 7: Summary / CTA slide
- Each slide: maximum 8-word headline + 1–2 sentence body
**Pass criteria:** Hook slide earns the swipe; each mistake is specific (not "don't undersell yourself" as a full slide); last slide has clear CTA

---

## TEST CASE 20: Departure Communication — Executive

**Input:** "I'm leaving my VP role after 4 years to start a company. Write a LinkedIn post."
**Platform:** LinkedIn
**Tone:** Warm Professional / CEO/Founder transition
**Modules expected:** writing-engine, tone-intelligence, reputation-protection, platforms/linkedin, quality-control
**Expected output characteristics:**
- Leads with what is being moved toward (not away from)
- Specific acknowledgment of the organization without formula
- Brief and intentional
- No "it's been an honor and a privilege" formula
- No scores to settle
**Pass criteria:** Genuine tone; specific acknowledgment; forward-looking; under 200 words

---

## TEST CASE 21: AMA Post — Reddit

**Input:** "Write my Reddit AMA post. I'm a former FDA regulator who now consults on pharmaceutical approvals."
**Platform:** Reddit
**Tone:** Intellectual/Thought Leader
**Modules expected:** writing-engine, platforms/universal-platforms [Reddit section], tone-intelligence, quality-control
**Expected output characteristics:**
- Title: factual, not promotional
- Opening: 3–5 sentences maximum; who, what, why this AMA
- No self-promotional language
- Sets clear window for answers
**Pass criteria:** Reads as genuine expertise offer; no corporate language; specific enough that users know what questions are appropriate

---

## TEST CASE 22: Multilingual — ID to EN Thought Leadership

**Input:** "Terjemahkan ini ke English untuk audiens LinkedIn internasional: 'Banyak pemimpin lupa bahwa otoritas bukan diraih dari jabatan, melainkan dari kepercayaan yang dibangun satu keputusan pada satu waktu.'"
**Platform:** LinkedIn
**Task:** Translate + adapt
**Modules expected:** intelligence/multilingual-communication, rewriting-engine, platforms/linkedin, quality-control
**Expected output characteristics:**
- Translated meaning-first (not word-for-word)
- English professional register appropriate for LinkedIn
- Maintains the original philosophical weight
**Pass criteria:** Native English speaker would not recognize it as translated; meaning is preserved; LinkedIn-appropriate register

---

## TEST CASE 23: Luxury Brand Instagram Caption

**Input:** "Caption for a new watch photo. The watch costs $12,000. Our brand is for serious collectors."
**Platform:** Instagram
**Tone:** Luxury/Premium
**Modules expected:** writing-engine, tone-intelligence [Luxury/Premium], platforms/instagram, quality-control
**Expected output characteristics:**
- No exclamation points
- Restraint and understatement
- Specific craft detail if available; request if not
- Short (under 80 words)
- No price mention unless strategically appropriate
**Pass criteria:** Reads as premium brand; no exclamation points; no hollow superlatives; specific detail present

---

## TEST CASE 24: YouTube Script Introduction — Authority Build

**Input:** "Write the intro for a YouTube video about the 3 biggest mistakes founders make when hiring their first VP of Sales."
**Platform:** YouTube
**Tone:** Intellectual/Thought Leader
**Task:** Script section
**Modules expected:** writing-engine, tone-intelligence [Intellectual], platforms/youtube, quality-control
**Expected output characteristics:**
- First 30–60 seconds of script
- Hook in first 5 seconds
- Credibility establishment (specific, not credential list)
- Preview of what the video covers
- Viewer retention through implied promise
**Pass criteria:** Would hold viewer attention past 30-second drop-off; credibility established through specific experience; does not ask for subscribe before delivering value

---

## TEST CASE 25: Tone Transformation — Corporate to CEO

**Input:** "We are pleased to announce that our company has successfully completed the acquisition of [Company X], which will enable us to expand our market presence and deliver enhanced value to our stakeholders."
**Task:** Rewrite — Transform to CEO/Founder tone
**Platform:** LinkedIn
**Modules expected:** rewriting-engine, tone-intelligence [CEO/Founder], platforms/linkedin, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Same information, completely different tone
- CEO/Founder: short, decisive, specific
- No "pleased to announce"; no "enhanced value"; no "stakeholders"
- Specific outcome named
**Pass criteria:** Tone unmistakably CEO/Founder; original information preserved; no banned phrases; quality score ≥ 85

---

## TEST CASE 26: Below-Quality Escalation

**Input:** User provides three words: "marketing tips post"
**Task:** Create
**Platform:** Unspecified
**Expected behavior:**
- System cannot produce quality output from three words
- Request critical missing information: platform, audience, specific topic angle, tone
- Maximum two clarifying questions before attempting with defaults
**Pass criteria:** System asks targeted questions; does not produce generic "marketing tips" content with no brief; if forced to proceed with defaults, clearly states assumptions made

---

## TEST CASE 27: Reputational Risk — Competitor Criticism

**Input:** "I want to post about why our competitor's product is inferior to ours. Their battery life is 30% shorter according to public benchmarks."
**Task:** Protect + Advise
**Platform:** LinkedIn
**Modules expected:** reputation-protection, recommendation-engine, quality-control
**Expected output characteristics:**
- Risk assessment for comparative claims
- Flag: legal risk for defamation if benchmark source is not cited
- Flag: reputational risk for direct competitor criticism
- Alternative: position own strengths without naming competitor
**Pass criteria:** Risk report identifies defamation risk; provides compliant alternative that achieves same positioning goal without the risk

---

## TEST CASE 28: Newsletter Introduction — Substack

**Input:** "Write the opening for my monthly newsletter for startup founders. Topic this month: how to manage board expectations during a down round."
**Platform:** Substack newsletter
**Tone:** Warm Professional
**Modules expected:** writing-engine, tone-intelligence [Warm Professional], platforms/universal-platforms, anti-ai-slop-engine, quality-control
**Expected output characteristics:**
- Opening paragraph earns the read (not "Dear subscribers...")
- Topic framing establishes why this month's topic matters now
- Warm but not soft — this is a difficult topic for founders
- 150–250 words for the opening section
**Pass criteria:** Opening would make a founder dealing with a down round feel understood and want to keep reading

---

## TEST CASE 29: Thought Leadership Positioning — C-Suite

**Input:** "I want to be known as a thought leader in AI ethics in the financial services industry. I'm a Chief Risk Officer. What should I post about?"
**Task:** Advise
**Platform:** LinkedIn
**Modules expected:** intelligence/personal-branding, recommendation-engine, intelligence/content-strategy, intelligence/audience-psychology
**Expected output characteristics:**
- Specific content angles at the intersection of AI ethics + financial services + CRO perspective
- What no one else is saying in this space
- 10 specific post ideas with hooks
- Platform strategy for building this positioning
**Pass criteria:** Angles are specific to the intersection (not generic "AI ethics" or generic "financial services"); CRO perspective is the differentiated angle; hooks are compelling

---

## TEST CASE 30: Full Ecosystem Test — Complex Multi-Module

**Input:** "I'm an Indonesian fintech founder who just closed a Series B ($15M). I want to post about it on LinkedIn in both English and Indonesian. The tone should fit my personal brand — I'm known for being direct, data-driven, and a bit irreverent."
**Platform:** LinkedIn (two versions)
**Tone:** CEO/Founder (with irreverent modifier)
**Modules expected:** ALL relevant modules — writing-engine, tone-intelligence, intelligence/executive-communication, intelligence/multilingual-communication, platforms/linkedin, anti-ai-slop-engine, reputation-protection, quality-control
**Expected output characteristics:**
- Two posts: one English, one Indonesian
- Both: not "excited to announce" openers
- English: CEO/Founder tone with distinctive personal voice
- Indonesian: modern professional Bahasa, culturally calibrated, maintains the irreverent note where appropriate
- Both posts: specific amount mentioned ($15M or IDR equivalent)
- Both posts: what this enables (not just what it is)
**Pass criteria:** Both posts score ≥ 85; both read as the same person in different languages; tone is consistent with "direct, data-driven, irreverent"; no hollow enthusiasm

---

## RELATIONSHIP TO OTHER MODULES

- `tests/quality-benchmarks.md` — scoring rubric for pass/fail criteria
- `tests/evaluation-protocol.md` — testing methodology
- All active modules — each test case exercises specific module combinations
