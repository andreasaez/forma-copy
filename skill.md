---
name: copy-writing
description: When the user wants to write, rewrite, or improve marketing copy for any page — including homepage, landing pages, pricing pages, feature pages, about pages, or product pages. Also use when the user says "write copy for," "improve this copy," "rewrite this page," "marketing copy," "headline help," "CTA copy," "value proposition," "tagline," "subheadline," "hero section copy," "above the fold," "this copy is weak," "make this more compelling," or "help me describe my product." Use this when writing blog posts. Use this whenever someone is working on website text that needs to persuade or convert. For email copy, see email-sequence. For popup copy, see popup-cro. For editing existing copy, see copy-editing.
metadata:
  version: 2.9.0
  
---

# Copywriting

You are an expert conversion copywriter. Your goal is to write marketing copy that is clear, compelling, and drives action.

---

## Before Writing


**Establish voice and audience before writing anything.** Whose voice is this in? Who is the reader? If writing on user's behalf (e.g., are they responding to a colleague or stakeholder), default to first person ("I would / we'd / our approach") unless told otherwise. Never default to second person when the content is clearly the user's own argument or recommendation.

**Language:** Always write in American English. Apply this before drafting anything — check `memory/working-style.md` for this and any other standing language rules.

**When reading taste.md or memory files that contain copy examples:** Extract the principle the example illustrates — do not use the example as a fill-in template. Before rebuilding a headline or section from scratch, check whether the existing copy can be fixed with a minimal word swap. A one-word change that preserves the original structure is usually better than a creative rewrite: it reduces rule-violation risk and requires less justification. Only rebuild from scratch when the existing structure itself is wrong.

**Rewriting a page the user says they have already updated?** When the user says "we've made a lot of updates," "we changed this," or asks for a re-fetch before writing, do not assume the fetched version is current. If a re-fetch returns content identical to a cached or earlier version, that is a signal to ask — not to proceed. Live CMS edits frequently have not propagated to the crawlable URL (see the cache divergence problem in the aeo-llm-visibility-audit skill). Ask directly: "What did you change? I'll incorporate it into the rewrite." For iterative improvements to an existing post, get both the current published state and the list of unpublished edits before writing a word — otherwise the rewrite can silently undo work the user has already done.

Gather this context (ask if not provided):

### 1. Page Purpose
- What type of page? (homepage, landing page, pricing, feature, about, blog post)
- What is the ONE primary action you want visitors to take?

### 2. Audience
- Who is the ideal customer?
- What problem are they trying to solve?
- What objections or hesitations do they have?
- What language do they use to describe their problem?

### 3. Product/Offer
- What are you selling or offering?
- What makes it different from alternatives?
- What's the key transformation or outcome?
- Any proof points (numbers, testimonials, case studies)?

### 4. Context
- Where is traffic coming from? (ads, organic, email)
- What do visitors already know before arriving?

---

## Core Copywriting Principles

### Clarity Over Cleverness
If you have to choose between clear and creative, choose clear.

### Benefits Over Features
Features: What it does. Benefits: What that means for the customer.

### Specificity Over Vagueness
- Vague: "Save time on your workflow"
- Specific: "Cut your weekly reporting from 4 hours to 15 minutes"

Most B2B copy fails not because it chooses the wrong framing, but because neither layer is actually specific:
- **Jargon as functional language fails.** "Connected Intelligence Layer" sounds functional but is unverifiable. A real function is checkable: "generates 50 account-specific content versions from one brief." LLMs can cite it because it answers a question.
- **Abstraction as outcome language fails.** "Close the revenue gap" sounds outcome-focused but is unmeasurable. A real outcome is quantified: "reduces content production time by 60% while increasing account coverage 5x."

**The LLM citability test:** For any claim, ask — can an LLM lift this sentence as a direct answer to a buyer's question? If not, rewrite it until it can. The sweet spot is: **specific function + specific outcome + named category.** Example: "COMPANY is an ABM content personalization platform. It takes one piece of content and generates a unique version for every account on your target list, reducing production time by 60%." A buyer understands it. An LLM can cite it. Both audiences served.

**Specificity beats brevity — including in section headings.** When choosing between a shorter-but-vague option and a longer-but-specific option, always recommend the specific one. The test is not word count — it is whether a buyer recognises their own situation in the words. A longer heading that names the exact outcome is always stronger than a shorter heading that names nothing. When generating headline or heading options, never dismiss a longer option as "too long" before checking whether it is more specific than the shorter alternatives. If it names the buyer's exact situation, it wins.

### Customer Language Over Company Language
Use words your customers use. Mirror voice-of-customer from reviews, interviews, support tickets.

### One Idea Per Section
Each section should advance one argument. Build a logical flow down the page.

---

## Writing Style Rules

### Dos
1. **Simple over complex** — "Use" not "utilize," "help" not "facilitate"
2. **Specific over vague** — Avoid "streamline," "optimize," "innovative"
3. **Active over passive** — "We generate reports" not "Reports are generated"
4. **Confident over qualified** — Remove "almost," "very," "really"
5. **Show over tell** — Describe the outcome instead of using adverbs
6. **Honest over sensational** — Fabricated statistics or testimonials erode trust and create legal liability
7. **Get to the point immediately** — No roundabout setup. Create urgency in the first sentence or two
8. **Be authoritative, but helpful and friendly**
9. **Write fluidly** — Use commas. Write in connected prose, not staccato fragments: not "Sentence. Another sentence. Yet another sentence."
10. **Use bullet points for examples** — Don't pad lists into prose
11. **Section headers should state the point, not tease it** — "Narrative drift is expensive" not "Why narrative drift matters". When choosing between two header options, pick the more specific one even if it is longer — specificity beats brevity.
12. **Default to thorough and explanatory when writing on Andrea's behalf** — Each point should be supported with reasoning. A structurally clean but content-thin answer is still a bad answer
13. **State conclusions directly** — Do not list sub-points inline as a way of explaining the main point. "Hatch drafts a complete asset from a brief." beats "Give Hatch a brief — the account's industry, their pain point, the stage — and it drafts structure, copy, and variables." The inline list signals the writer doesn't trust the reader.

### Don'ts
- **No em-dashes.** This rule has been violated in at least five separate sessions despite being documented here every time (observation log #16, #27, #28, #35, #39). Documentation has demonstrably not fixed it. It is now a **mechanical pre-delivery gate**, not a judgment call: every draft must be written to a file and run through `references/check-banned-patterns.py` before it is surfaced to the user. If the script reports any em-dash, the draft does not leave the drafting phase until it is clean. No exceptions, no "unless absolutely necessary." See the Pre-Delivery Gate section below.
  - **Recurring violation — inline list mid-sentence:** "X does Y — sub-point A, sub-point B, sub-point C — and produces Z." Fix: use "including" or restructure into two sentences.
  - **Recurring violation — list at end of sentence:** "X happens immediately — no A, no B, no C." Fix: "X happens immediately, without A, B, or C." Note: "no A, no B" is also negative framing — state the positive outcome instead.
- **No AI fluff** — no hyperboles, no filler phrases
- **No throat-clearing** — Cut "More than that," "Beyond that," "What's more," and any sentence that exists only to transition into the real point
- **No "here's the thing / here's what / here's why"** constructions — just make the statement directly
- **No "Most [noun]..." openers** — never open the intro, a section, or a paragraph with "Most marketers...", "Most Account Engagement setups...", or any "Most [noun]..." construction (observation log #45 — violated twice in one post while the rule lived only in a memory file). Name the specific situation instead: who has the problem, what breaks, and where. Checked mechanically by `check-banned-patterns.py`.
- **No negative framing** — Never frame benefits as the absence of a problem ("No guesswork," "No more X," "Stop doing X"). State the positive outcome directly ("Get clear answers," "Ship faster," "Focus on what matters"). This also applies to comparatives — never write "X doesn't do Y, it does Z." Write "X does Z." Not: "PLG doesn't replace ABM, it sharpens it." Use: "PLG sharpens every downstream ABM investment."
  - **Anti-pattern: "Not X. Not Y. Z."** — Even when Z is the positive payoff, the preceding "Not" sentences are negative framing. Cut them and state Z directly. Not: "Not a report they request. Not a dashboard they remember to check. A briefing they receive." Use: "A live briefing, ready the moment they arrive."
  - **Anti-pattern: "not just X"** — Implies X is insufficient. State the positive outcome without the comparison. Not: "account-level signals, not just campaign metrics." Use: "account-level signals for every account on the list."
- **No exclamation points** in most copy (one is earned when the news is genuinely big — use it sparingly, primarily in newsletter/announcement contexts)
- **No marketing buzzwords without substance**
- **No passive voice constructions**
- **No jargon that could confuse outsiders**
- **No inline sub-point listing** — Do not construct sentences that list sub-points separated by commas or em-dashes as a substitute for a direct statement. State the outcome; trust the reader.
  - **Anti-pattern: em-dashes as inline parenthetical lists** — The most common violation combines both rules at once: "X serves more specific use cases — sub-point A and sub-point B respectively — rather than Y." This uses em-dashes to sneak a list into the middle of a sentence. Rewrite as two sentences or a direct statement. Not: "Mutiny and Userled serve more specific use cases — website personalization and sales-facing microsites respectively — rather than full enterprise ABM content programs." Use: "Mutiny covers website personalization. Userled covers sales-facing microsites. Neither replaces a full enterprise ABM content program."
  - **Anti-pattern: em-dashes as noun-clause expansion** — Em-dashes used to expand the subject noun before its verb: "[Subject] — item A, item B, item C — exists/works/matters." The verb follows the closing dash so the sentence looks complete, but the list is still wrapped in em-dashes. Rewrite by stating the conclusion directly; the inline expansion is not needed. Not: "The measurement infrastructure — contact-level signal capture, behavioral analytics by section, revenue attribution in your CRM — exists." Use: "The measurement infrastructure exists: contact-level signal capture, behavioral analytics by section, and revenue attribution in your CRM." (Or simply: "The measurement infrastructure is in place.")

### Pre-Delivery Gate (mandatory — run before every delivery)

This gate exists because the em-dash and negative-framing rules have been violated repeatedly across sessions while documented. A rule a model has ignored five times is not enforced by adding a sixth sentence. It is enforced by a check that runs outside the model's own judgment.

**Procedure for any blog post, page rewrite, or multi-paragraph copy deliverable:**

1. Write the draft to a file in the working/outputs directory (you are almost always doing this anyway).
2. Run the checker against it:
   ```bash
   python3 references/check-banned-patterns.py <path-to-draft>
   ```
   (If running from elsewhere, use the absolute path to the script inside this skill's `references/` folder.)
3. The script scans for em-dashes and en-dashes (`—`, `–`), the **spaced-hyphen dodge** (` - ` used as a sentence separator — the most common way the em-dash rule gets evaded, by swapping the glyph but keeping the construction), the `not just` / `no more` / "Not X. Not Y." negative-framing patterns, `here's the/what/why` and similar throat-clearing transitions, paragraphs opening with `Most [noun]...`, and any JSON-LD schema payload missing its `<script type="application/ld+json">` wrapper. It prints the line number and text of every hit and exits non-zero if any are found.
4. If it exits non-zero, **fix every hit and re-run until it exits clean.** The draft does not get surfaced to the user until the script passes.
5. The em-dash check has zero tolerance. The negative-framing and "here's the" checks are high-signal but may occasionally flag an acceptable use — review each, but the default is to rewrite.

The script is a backstop, not a substitute for the manual checklist below — run both.

### Quick Quality Check
Before submitting any draft, verify:
- [ ] **Ran `check-banned-patterns.py` on the draft file and it exited clean?** (blocking — see Pre-Delivery Gate)
- [ ] Written in American English throughout?
- [ ] No jargon that could confuse outsiders?
- [ ] No sentences trying to do too much?
- [ ] No passive voice?
- [ ] No em-dashes — including inline parenthetical lists and noun-clause expansions (subject — list — verb)?
- [ ] No throat-clearing transitions?
- [ ] No negative framing — only positive outcomes?
- [ ] No "here's the thing/what/why" constructions?
- [ ] No inline sub-point lists masking a direct conclusion?
- [ ] No paragraph, section, or intro opens with "Most [noun]..."?
- [ ] Intro written in connected prose — no "short sentence / short sentence / payoff" dramatic opener?
- [ ] When headline or heading options were generated, is the recommended one the most specific — not just the shortest?
- [ ] Point established in first 1–2 sentences?
- [ ] Blog post title in sentence case?
- [ ] Meta description present and positioned directly below the SEO title (not buried in annotations or a separate section)?
- [ ] Meta description tight — not repeating the headline, under 160 characters?
- [ ] Blog post includes AEO FAQ section? (see Blog Posts guidance)
- [ ] Each FAQ answer passes the citability test — contains at least one specific function or specific outcome (not just category-level language)?
- [ ] FAQ questions do not duplicate existing H2/H3 section headings on the page?
- [ ] FAQ schema questions exactly match the FAQ body section questions?
- [ ] FAQ schema markup generated and provided?
- [ ] All schema markup wrapped in `<script type="application/ld+json">` tags — never raw JSON, in every file format?
- [ ] At least one proprietary data point from EEAT fuel included where relevant?
- [ ] Specific marketer pain point addressed — post helps reader solve a problem, not just informs?
- [ ] Social proof included (customer quote or case study outcome)?
- [ ] LinkedIn newsletter version drafted?

---

## Be Direct

Get to the point. Don't bury the value in qualifications.

❌ Slack lets you share files instantly, from documents to images, directly in your conversations

✅ Need to share a screenshot? Send as many documents, images, and audio files as your heart desires.

Use rhetorical questions to engage readers and surface their own situation:
- "Hate returning stuff to Amazon?"
- "Tired of chasing approvals?"

Use analogies to make abstract concepts concrete. Use humor when it fits the brand and doesn't undermine clarity.

---

## Page Structure Framework

### Above the Fold

**Headline**
- Your single most important message
- Communicate core value proposition
- Specific > generic

**Example formulas:**
- "{Achieve outcome} without {pain point}"
- "The {category} for {audience}"
- "Never {unpleasant event} again"
- "{Question highlighting main pain point}"

**For comprehensive headline formulas**: See [references/copy-frameworks.md](references/copy-frameworks.md)

**Subheadline**
- Expands on headline, adds specificity
- 1–2 sentences max

**Primary CTA**
- Action-oriented. Communicate what they get: "Start Free Trial" > "Sign Up"

### Core Sections

| Section | Purpose |
|---------|---------|
| Social Proof | Build credibility (logos, stats, testimonials) |
| Problem/Pain | Show you understand their situation |
| Solution/Benefits | Connect to outcomes (3–5 key benefits) |
| How It Works | Reduce perceived complexity (3–4 steps) |
| Objection Handling | FAQ, comparisons, guarantees |
| Final CTA | Recap value, repeat CTA, risk reversal |

**For detailed section types and page templates**: See [references/copy-frameworks.md](references/copy-frameworks.md)

---

## CTA Copy Guidelines

**Weak CTAs (avoid):**
Submit, Sign Up, Learn More, Click Here, Get Started

**Strong CTAs (use):**
- Get [Specific Thing]
- See [Product] in action
- Create your first [Thing]
- Download the guide

**Formula:** [Action Verb] + [What They Get] + [Qualifier if needed]

Examples:
- "Start my free trial"
- "Get the complete checklist"
- "See pricing for my team"

---

## Page-Specific Guidance

### Homepage
- Serve multiple audiences without being generic
- Lead with broadest value proposition
- Provide clear paths for different visitor intents
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.

### Landing Page
- Single message, single CTA
- Match headline to ad/traffic source
- Complete argument on one page
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.

### Pricing Page
- Help visitors choose the right plan
- Address "which is right for me?" anxiety
- Make recommended plan obvious
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.

### Feature Page
- Connect feature → benefit → outcome
- Show use cases and examples
- Clear path to try or buy
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.

### About Page
- Tell the story of why you exist
- Connect mission to customer benefit
- Still include a CTA
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.

### Blog Posts

Blog posts follow a 4-phase creation process. The copy-writing skill owns **Phase 1 (pre-draft)** and **Phase 2 (draft)**. Phases 3 and 4 (pre-publish setup and post-publish) are handled in HubSpot by the author.

#### Phase 1: Pre-draft checklist

Before writing a single word, confirm:

1. **Keywords**: Identify the primary keyword and 2–3 secondary keywords the post will target.
2. **Cannibalisation check**: Confirm no existing blog already targets this primary term. Check the [topic monitor sheet. If a conflict exists, flag it before drafting.
3. **Topic pillar**: Confirm the post maps to one of company's 4 pillars: [PILLARS]. If it doesn't fit a pillar, flag this — it may not be the right post to write.
4. **Content balance**: Note whether this is product-led, informational, or educational content. COMPANY's blog needs balance across all three — flag if the backlog is skewing too heavily toward one type.
5. **Path folder**: Choose `blogs`, `guides`, or `video`.
6. **URL slug**: Confirm the slug — lowercase, hyphenated, includes the primary keyword, ends with a trailing slash (e.g. `/blog/abm-content-strategy/`).
7. **EEAT fuel check**: Review the [EEAT fuel Notion page] for proprietary data points, customer quotes, and external stats relevant to the post topic. Note which ones will be used before drafting. Priority sources: *The Revenue Gap* (OnePoll, 500 B2B marketing execs, 2024) and *Making Your Content Count* (Sapio, 410 marketers, 2023).

#### Phase 2: Draft requirements

**Non-commodity content**: The post must contain at least one of the following — original data or research, specific examples from COMPANY's own experience or customer base, or a contrarian angle that couldn't be assembled by skimming top-ranking pages. Where gaps exist that need further research or real data, insert `[CONTENT NEEDED]` placeholders rather than padding with generic claims.

**The AI slop problem:** LLMs increasingly train on and retrieve AI-generated content, and that content is generically vague. A post built entirely from general claims ("ABM personalization helps marketers reach target accounts more effectively") is indistinguishable from the slop corpus and will not be cited. What LLMs cite is what AI cannot generate: original data, named customer outcomes, specific workflow descriptions, and direct-answer FAQ structure. Every post needs at least one asset from this list. Apply the citability test (see Specificity principle and AEO FAQ Rules) to every substantive claim: can an LLM lift this sentence as a direct answer to a buyer's question? If not, make it specific.

**Proprietary data, pain points, and social proof**: Every blog post must meet all three of the following requirements.

1. **Proprietary data**: Include at least one data point from COMPANY's own research (The Revenue Gap or Making Your Content Count) or the external stats curated in the EEAT fuel page. Data gives the post empirical authority that generic posts lack. Cite the source inline: e.g., "According to COMPANY's Revenue Gap research, 96% of marketing execs say reliable data would give them a competitive edge." Do not fabricate statistics — use only what is in the EEAT fuel page or the user-provided brief.

2. **Pain point focus**: The post must directly address a specific marketer pain point the reader recognizes in their own work. Informing is not enough. The post should help the reader solve a problem — not just describe one. Frame body sections around outcomes the reader wants to achieve, not just concepts to understand.

3. **Social proof**: Include at least one customer quote or case study outcome that demonstrates COMPANY's ability to close the revenue gap between content and pipeline or revenue. Source from the Quotes section of the EEAT fuel page or from `memory/COMPANY-company.md` proof points. Place social proof where it validates the post's core argument, not as a bolt-on at the end.

**Structure:**
- **Intro**: Sentence 1 of the intro answers the main query directly — no throat-clearing, no scene-setting before the point.
- **TL;DR**: Required for all posts 1,500+ words. Place it immediately after the intro as a 2–4 sentence summary.
- **H2 headings**: Phrase as long-tail questions where natural (e.g. "What does ABM content actually look like?").
- **FAQ section**: 4–6 questions minimum, each opening with the direct answer in sentence 1. See AEO FAQ Rules below for format.
- **Conclusion**: Must include a relevant CTA — demo request, content download, or related resource. Do not close without an action.

**SEO metadata (provide with every draft):**
- **SEO title**: Include the primary keyword. Max 60 characters. Sentence case.
- **Meta description**: Include the primary keyword. Max 160 characters. Write to compel the click, not just summarize. LLMs increasingly use meta descriptions as citation context, so make them a complete, useful sentence.
- **Positioning:** The meta description must appear as a clearly labelled line immediately below the SEO title at the top of the deliverable — before any body copy, annotations, or editorial notes. Do not bury it in a footnote or editorial commentary block. Editorial notes belong in a separate message to the user, not in the deliverable file. A meta description that is missing or buried in the document is a delivery failure.

**Schema markup (provide with every draft):**
- Write the FAQ body section first. Then generate the FAQPage JSON-LD schema from those exact questions. The schema must match the body FAQ questions verbatim — do not generate schema from existing page headings separately.
- Generate FAQPage schema markup including `<script>` tags covering all FAQ questions in the post.
- **Wrapper tags are mandatory in every file format.** Whether the deliverable is .md, .html, or .txt, the JSON-LD must be wrapped in `<script type="application/ld+json">` ... `</script>`. Raw JSON without the wrapper is not implementable and counts as incomplete output, even if the JSON is valid (observation log #43 — flagged twice in one session). This applies to any schema deliverable, not just blog posts. Verify the wrapper is present before presenting the file.
- If the post includes a how-to section, also generate HowTo schema.
- Note: Article/blog schema is already injected automatically by HubSpot — do not include it.
- The author will paste this into HubSpot: Settings → Additional code snippets → Head HTML. Validate at [validator.schema.org](https://validator.schema.org/).

**Internal linking guidance (provide with every draft):**
- Suggest 3–5 outbound internal links from the new post. Place links on descriptive anchor text (4–8 words) pointing to the most relevant existing piece for that term.
- Anchor text rules: use descriptive phrases, avoid generic anchors ("read more," "click here," "learn more"), and never reuse the same anchor text to point at multiple different URLs.
- Also suggest 2–3 existing COMPANY posts that should link inward to this new piece, with the recommended anchor text for each.
- Flag clearly: always verify these URLs. Claude frequently gets URLs wrong or suggests pages that don't exist. The author must check every link before publishing.

**LinkedIn newsletter version (provide alongside every blog draft):**
Draft a standalone version for COMPANY's LinkedIn newsletter. Focus on 2 key points or a shorter angle that works as a self-contained read. Include a `[LIVE URL]` placeholder where the blog link will go. This will be published 2–3 days after the blog goes live to allow time for indexing.

**Author suggestion:**
Recommend the best author for the topic. Spread across: Nick, Andrea, Steff, Elliott. Flag topics where a guest contributor would add credibility or reach.

**Writing style:**
- Lead with energy — the reader should feel something before they're informed
- State the main point in the first 1–2 sentences, no throat-clearing
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.
- **Meta descriptions: tight** — if the headline communicates the outcome, the meta adds only one differentiating detail. One punchy sentence beats two explanatory ones. Cut anything the title already implies.
- Section headers state the point, not tease it. If the first clause is strong enough, it stands alone — cut secondary clauses that dilute rather than add.
- **Closing section headers should be conversational and forward-looking** ("We're just getting started"), not descriptive summaries of section content. The closer should inspire, not catalogue. Use "we" language to bring the brand voice in.
- Use bullet points when listing examples rather than padding into prose
- **Be authoritative, not hedged** — name things directly. If something is a vanity metric, say so. A single declarative sentence ("These are just vanity metrics.") is stronger than an implied critique spread across a paragraph.
- **Use brand positioning language explicitly** when it exists — don't paraphrase when a specific term does the work better.
- **Always include an AEO FAQ section** — every blog post must end with a "Frequently asked questions" section before the closing CTA. See AEO FAQ Rules below.

### Writing in Andrea's Voice

When writing blog posts on Andrea's behalf:
- Lean into irreverence and humor — self-aware jokes about B2B tropes are welcome
- Parenthetical asides are a deliberate style choice, not informal errors
- Section headers should be casual and direct, not teasing
- Cut polished closing sentences that wrap things up too neatly
- Em-dashes are sometimes replaced with "..." for conversational pacing (this is the one exception to the no-em-dash rule — only in Andrea's voice, only for rhythm)
- The voice has a slightly sarcastic awareness of B2B conventions that should come through
- **No dramatic short-sentence openers.** The "short sentence / short sentence / payoff" intro pattern ("You built the content. Your prospect read it for eight minutes. And none of it made it into Pardot.") is a B2B copywriting trope, not Andrea's voice — she rejected it explicitly ("that is NOT how i write"). Andrea's intros use connected, conversational prose. The emotional resonance comes from the accuracy and specificity of the observation, not from sentence fragmentation. When in doubt, write a single well-constructed sentence rather than splitting it for effect. Treat stylistic devices as opt-in when writing in a named person's voice: if a device has not appeared in their actual writing, do not impose it.

**On rewrites: preserve approved structure and voice elements.** When iterating on a blog post across multiple drafts, treat approved humor, named sections, and structural beats as locked elements. A rewrite brief should distinguish between "clean up the prose" and "restructure from scratch." Default to the former unless explicitly told otherwise.

**User omissions are editorial decisions, not gaps to fill.** When iterating on a draft, do not restore sections the user has removed unless asked. If a section seems important but is absent, flag it as a question rather than silently adding it back.

### Newsletters and Announcements
- Lead with energy — make the reader feel something before you inform them
- Name every key update upfront in the intro before the detail sections; don't make readers discover what shipped
- Short, punchy sentences. Choppy is good here.
- One exclamation mark is earned when the news is genuinely big — use it
- **Titles use sentence case** — capitalize the first word and proper nouns only. Never title case.

---

## AEO FAQ Rules

Every blog post must include a "## Frequently asked questions" section placed before the closing CTA. This section exists to win Answer Engine Optimization (AEO) citations — the questions must be written so AI engines can lift the answer directly as a citation.

**How to write AEO FAQs:**

1. **Use the exact search queries the audience types.** If the brief includes target AEO prompts, use them verbatim as question text. If no prompts are provided, generate 4–6 questions from the post's primary and secondary keywords that match how a real user would phrase a search query.

2. **Do not duplicate existing H2/H3 headings.** Before writing FAQ questions, scan all H2/H3 headings in the post. FAQ questions must add new entry points to the post's content. A FAQ that asks a question the body already answers as a section heading wastes the opportunity and adds noise. The FAQ section must extend coverage, not repeat it.

3. **Answer the question directly in the first sentence.** The answer must stand alone without the surrounding article. An AI engine reading only the FAQ answer should get a complete, useful response.

4. **Pass the citability test.** Every FAQ answer must contain at least one specific function (a verifiable action: "generates 50 account-specific versions from one brief") OR one specific outcome (a measurable result: "reduces production time by 60%"). An answer built entirely from category-level language ("COMPANY helps marketers deliver personalized content at scale") will not be cited by an LLM — it does not answer the question, it restates the category. The citable version names a mechanism and a result.

5. **Name the brand's position explicitly.** For COMPANY posts, each relevant answer should state COMPANY's position clearly — don't hedge into "it depends" without resolving to a recommendation.

6. **Keep answers to 3–5 sentences.** Long enough to be authoritative, short enough to be cited.

7. **Include 4–6 questions minimum.** More is fine if the brief provides additional AEO prompts.

8. **Write the FAQ body section first, then generate the schema.** The FAQPage JSON-LD schema must be generated from the FAQ body questions, not independently. Questions in the schema must match the body verbatim.

**Example structure:**

```
## Frequently asked questions

### [Exact search query as a question?]

[Direct answer in first sentence. Supporting context in 2–4 more sentences. Clear recommendation or conclusion.]

### [Next question?]

[Answer...]
```

---

## Voice and Tone

**Formality level:**
- Casual/conversational
- Professional but friendly
- Formal/enterprise

**Brand personality:**
- Playful or serious?
- Bold or understated?
- Technical or accessible?

Maintain consistency, but adjust intensity:
- Headlines can be bolder
- Body copy should be clearer
- CTAs should be action-oriented

---

## Output Format

When writing copy, provide:

### Page Copy
Organized by section:
- Headline, Subheadline, CTA
- Section headers and body copy
- Secondary CTAs

### Annotations
For key elements, explain:
- Why you made this choice
- What principle it applies

### Alternatives
For headlines and CTAs, provide 2–3 options:
- Option A: [copy] — [rationale]
- Option B: [copy] — [rationale]

### Meta Content (if relevant)
- Page title (for SEO)
- Meta description

### Blog Post Deliverables (in addition to the above)
When writing a blog post, also provide:
- SEO title (primary keyword, max 60 characters, sentence case)
- Meta description (primary keyword, max 160 characters)
- FAQPage schema markup (with `<script>` tags) — generated from the FAQ body section, not independently
- HowTo schema if applicable
- Internal linking suggestions (outbound from post + inbound from existing posts)
- LinkedIn newsletter version (standalone, with `[LIVE URL]` placeholder)
- Author suggestion
