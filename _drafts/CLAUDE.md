# Claude Guidelines — _drafts/

Drafts are where the writing happens. Quality bar is high — every draft should be clean enough that publishing requires only minor tweaks.

## Writing Rules
- **750 words maximum.** Count words before finishing. Cut aggressively.
- **Define every technical term** the first time it appears, immediately and in plain language. Format: "term (plain-language definition)" or a short parenthetical or follow-on sentence.
- **Simple sentence structure.** Prefer short sentences. Avoid nested clauses. If a sentence needs to be read twice, rewrite it.
- **No jargon without explanation.** If a term can't be explained simply, question whether it needs to be in the article at all.
- **Active voice** wherever possible.

## Visual Opportunities
When writing, flag every place where a visual would help a non-technical reader more than prose. Use inline comments:
```
<!-- VISUAL OPPORTUNITY: [specific description — e.g., "flowchart showing how data moves from sensor to dashboard"] -->
```
Be specific. "A diagram" is not enough — describe exactly what it should show. Err on the side of flagging too many; the author will decide what to build.

## Grammar, Spelling & Usage Checklist
Run through this checklist before considering a draft complete:

**Spelling & Typos**
- [ ] All words spelled correctly (watch proper nouns, technical terms)
- [ ] No doubled words ("the the")
- [ ] Consistent spelling of any term used multiple times

**Punctuation**
- [ ] Commas used correctly (no comma splices, no missing Oxford commas in lists)
- [ ] Apostrophes correct (its vs. it's, possessives)
- [ ] Em dashes, en dashes, and hyphens used correctly
- [ ] No missing end punctuation
- [ ] Quotation marks consistent and correctly placed

**Grammar & Usage**
- [ ] Subject-verb agreement throughout
- [ ] Consistent tense (don't mix past and present)
- [ ] No dangling modifiers
- [ ] "That" vs. "which" used correctly
- [ ] "Who" vs. "that" for people
- [ ] Numbers: spell out one through nine, use numerals for 10+
- [ ] No sentence fragments (unless intentional for style)

**Clarity & Readability**
- [ ] Every technical term defined on first use
- [ ] No unexplained acronyms
- [ ] No sentences that need to be read twice to understand
- [ ] Paragraph lengths vary — no wall-of-text paragraphs

**Word Count**
- [ ] Total word count confirmed at or under 750

## Jekyll Front Matter
Every draft should include front matter at the top, ready for publishing:
```yaml
---
layout: post
title: "Article Title"
date: YYYY-MM-DD
categories: [category]
---
```
Add `<!--break-->` after the first paragraph to set the excerpt.

## Draft File Naming
Use the format `YYYY-MM-DD-slug.md` when the draft is close to ready for publishing.
