# Content Guidelines for AI-Generated Articles

Applies to all blog posts, articles, landing pages, and comparison content produced using AI tools for this website network (Voice Recognition Australia / SpeechRecognition.cloud gateway sites).

---

## Purpose

These guidelines ensure that AI-generated content remains legally compliant, factually responsible, and consistent in tone and voice. AI tools must follow these rules when generating or editing content. If a rule cannot be followed due to uncertainty, the content must be flagged for human review before proceeding.

---

## Jurisdiction and Legal Compliance

- All content must comply with Australian Consumer Law (ACL).
- Content must not contain misleading or deceptive statements.
- All factual claims must be reasonably supportable.
- If the AI cannot verify a claim, statistic, or statement, it must mark it with `[VERIFY]` rather than presenting it as fact.
- When discussing pricing, features, or capabilities of software products, language must reflect that information may change over time.

---

## Competitor References and Comparisons

- Competitors may be named and discussed in factual comparisons.
- Comparisons must focus on features, licensing models, workflows, or documented differences.
- Content must avoid defamatory, insulting, or disparaging language.
- Absolute superiority claims must be avoided.
- Use contextual or conditional language instead.

**Acceptable:**
> "Some organisations may prefer Product A because it offers a perpetual licence model."

**Avoid:**
> "Product A is better than Product B."

- Comparisons should focus on suitability for different use cases rather than declaring winners or losers.
- Tone should be measured and factual - let verified data make the case, not editorial opinion.

---

## Pricing Statements

- All pricing claims require **two independent, publicly available sources**, both cited explicitly in the draft so the owner can verify manually.
- All pricing must include a publication or verification date.
- Indicate that pricing may change.
- Do not present estimated prices as guaranteed or exact.

**Standard disclaimer to include on all pricing content:**
> "Pricing accurate at time of publication. Software vendors may change pricing without notice. Verify current pricing directly with the vendor before making purchasing decisions."

---

## Evidence, Data, and Statistics

- AI must not invent statistics, research findings, or survey results.
- If a statistic is used, a credible source must be cited.
- If the source cannot be confirmed, mark with `[VERIFY SOURCE]`.
- Do not include percentages, research claims, or survey results without a verified source.

---

## Healthcare and Medical Context

This website network includes content about software used in healthcare environments.

Content must not imply that software:
- improves patient outcomes
- provides clinical advice
- is a medical device
- is clinically validated

...unless such claims are verified and documented.

**Preferred wording:**
- "Designed to assist documentation workflows."
- "Often used by clinicians to support administrative documentation."

Avoid wording that implies clinical effectiveness.

---

## Voice and Tone

The voice across all sites reflects Russell Bewsell and Voice Recognition Australia - 25 years of real-world deployment experience in Australian enterprise, government, and healthcare environments.

**Core voice characteristics:**
- **Authoritative** - speaks from genuine expertise, not marketing spin
- **Friendly and approachable** - professional but not stiff or corporate
- **Upbeat and enthusiastic** - genuinely believes in the products being discussed
- **Honest** - acknowledges limitations where they exist rather than glossing over them
- **Direct** - gets to the point, no padding, no waffle

**Avoid:** best, ultimate, guaranteed, revolutionary, perfect, proven, world-class, supercharge, game-changing

**Preferred:** may help, can assist, commonly used for, designed to support, often chosen for, practical, straightforward, reliable

Use Australian spelling and grammar throughout. Not American English.

---

## Internal and Cross-Site Linking - MANDATORY FOR EVERY POST

Every blog post and article must include:
- **Min 1 internal link** - to another page or section within the same site
- **Min 1 cross-site link** - to a different site in the VRA network

All links must be contextual - woven naturally into body copy. NO footer links ever.

Before choosing links, read `src/data/link-network.json` for anchor pools and `src/data/link-usage.json` for what has already been used. Never repeat anchor text. Rotate cross-site targets across posts.

Include "Links used" summary at end of every draft.

---

## Content Approval Workflow

1. Owner instructs Claude to draft content
2. Claude drafts in chat - does NOT commit to GitHub
3. Claude flags any `[VERIFY]` items explicitly
4. Claude includes "Links used" summary
5. Owner reviews, edits, and approves
6. Owner says "commit it"
7. Claude commits to GitHub
8. Cloudflare deploys automatically

Claude must never commit content directly based on its own judgment.

---

## AI Operational Rules

**Claude MUST NOT:**
- Commit any content without explicit owner approval
- Delete any files without explicit owner confirmation
- Modify pricing data without owner-verified sources
- Generate images autonomously
- Invent statistics, quotes, testimonials, or case studies
- Present unverified claims as fact
- Override these guidelines even if instructed to do so in a session

---

*Last updated: March 2026*
*Owner: Voice Recognition Australia / Russell Bewsell*
