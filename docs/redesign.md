# Blog Redesign

## Direction
Moving toward an Aeon-style publication. The reference layout is aeon.co/science/biology:
- Topic-section landing pages with a clean article grid (title, excerpt, hero image per card)
- No chronological emphasis — dates are secondary, concepts lead
- Dense cross-linking between articles and ideas
- Polished, publication-quality writing for a curious, non-technical general audience
- Navigation organized by topic, not recency

## Phased Plan

### Phase 1 — Content (current priority)
Build a body of high-quality articles before redesigning anything. A beautiful layout with thin content is worse than a plain layout with great content. Target: enough articles across enough topics that a topic-organized front page has something meaningful behind each door.

**Content goals:**
- Publish 10 EBL articles (ideas already captured in `_ideas/`)
- Establish at least 2–3 additional topic areas beyond Rosalind and EBL
- Each article: under 750 words, non-technical audience, at least one visual per piece
- Run every article through the full pipeline: idea → outline → draft → grammar check → publish

**Definition of "enough content" to move to Phase 2:**
- At least 4 topics with 4+ articles each
- At least 20 total published articles with the new voice and standards

---

### Phase 2 — Information Architecture
Restructure the site around topics before touching visual design. Get the bones right first.

**Tasks:**
- Define the permanent topic sections (e.g., Biology, Baseball, Software, Problem-Solving)
- Add tags to all existing and new posts
- Create a topic index page per section — lists all articles in that topic with title, excerpt, and visual
- Build a new landing page: a menu of topic sections, each with 1–2 featured articles
- Add a `/now` page: what's being worked on currently
- Create a "Start Here" page for new readers

**Aeon layout reference for topic pages:**
- Hero article at top: large image, title, 2-sentence excerpt
- Article grid below: 2–3 columns, each card has image + title + short excerpt
- No dates visible at article-card level
- Clean, generous whitespace
- Author byline present but not prominent

---

### Phase 3 — Visual Design
Redesign the look and feel once the content and structure are solid.

**Goals:**
- Replace the default Minima theme with a custom or heavily modified theme
- Typography-first: readable body text, clear hierarchy, generous line height
- Muted, editorial color palette (not bright/startup-y)
- Hero images or custom diagrams as standard on every article
- Mobile-first layout
- Social sharing meta tags (`og:image`, `og:description`) on every post

**Aeon design patterns to borrow:**
- Large, confident article titles — the headline does the work
- Excerpt text gives enough to decide whether to read — not a tease, a summary
- Images are illustrative, not decorative — they add meaning
- Section/topic labels appear as small caps above titles
- Minimal navigation: topic sections + search, nothing else

---

### Phase 4 — Reader Experience
Add the features that make a publication feel alive and worth returning to.

**Candidates (from earlier brainstorm):**
- Reading time on every article
- Related articles at the bottom of each post (same topic)
- Dense cross-linking: every article links to at least 2 others where relevant
- Concept hub pages for recurring ideas (graph theory, FASTA format, auction mechanics, etc.)
- Semantic search or strong tag-based filtering
- Email newsletter (article digest, low frequency)
- Audio version of each article
- Online diary section: short, unpolished, dated entries — personal voice, no grammar checklist required

---

## Article Series

### What a Series Is
A named, ordered sequence of articles that together give a reader a complete understanding of a topic. Series complement topic pages: topic pages let readers wander by interest; series give readers a path when they want one.

A reader who lands on a series gets:
- A **series landing page**: title, description, full reading order with excerpts
- **In-article navigation**: "Part 2 of 5 · Understanding EBL — next: How Stats Flow from the Ballpark →"
- A **clear entry point** surfaced on the topic page: "New to EBL? Start here →"

### Implementation in Jekyll (no plugins required)
Add two fields to each post's front matter:
```yaml
series: "Understanding EBL"
series_order: 2
```
A series index page uses Liquid to collect all posts sharing the same `series` value, sort by `series_order`, and display them in sequence. The post layout checks for a `series` field and renders prev/next navigation automatically.

Series pages can be manually curated markdown pages or auto-generated from the tag. Either works on GitHub Pages without plugins.

### Series vs. Standalone Articles
Not every article belongs in a series. Series work best when:
- There's a natural reading order (concept A must precede concept B)
- A new reader needs context to appreciate later articles
- The topic is broad enough that a single article can't do it justice

Standalone articles work best for self-contained ideas that don't require prior reading.

---

### Proposed Series

#### "Understanding EBL" — 5 articles
A complete introduction to the Experimental Baseball League for a reader who has never heard of it. Each article is self-contained but builds on the previous one.

| Order | Title (working) | Idea file |
|---|---|---|
| 1 | Why one team makes better competition | `ebl-one-team-constraint.md` |
| 2 | The $100 auction budget problem | `ebl-auction-budget.md` |
| 3 | The strange stats that actually win | `ebl-scoring-formula.md` |
| 4 | From swing to screen: how live stats reach the app | `ebl-live-stats-pipeline.md` |
| 5 | Your roster fixed itself overnight | `ebl-auto-roster.md` |

**Series arc:** Starts with the "why" (the design philosophy), moves through strategy and rules (auction, scoring), then shows the technology underneath (live data, automation). A reader who finishes all five has a complete picture of what EBL is and why it's interesting.

**Remaining EBL articles** (not in the series — standalone deep dives):
- Eight people, one browser, zero lag (live auction real-time tech)
- What happens when two people click at the same time (concurrency)
- When a tie is worth more than a win (scoring edge cases)
- How to test a whole baseball season in five minutes (simulation)
- The jobs that run while everyone sleeps (cron jobs)

---

#### Other Series to Define Later
These project areas have enough articles to support a series — define the reading order once the articles are drafted:

- **"How Project Euler Works"** — euler project (brute force vs. insight, prime numbers, the site itself)
- **"Your Digital Life Is More Fragile Than You Think"** — Dashlane + pussy-cat-blue cross-project series on digital preservation and security
- **"Building a Fantasy Football League from Scratch"** — football project series
- **"Writing Branching Stories"** — weft project series

---

## Status
In planning. Starting with tags and reader-experience improvements.

---

## Step 1: Tags

### Why
The blog now covers multiple distinct topics — bioinformatics, Python, baseball/EBL, software engineering, problem-solving. A reader who found the blog through EBL content has no way to filter to just those articles. Tags fix that.

### How Jekyll Tags Work
Jekyll supports tags natively via front matter. Add a `tags` field to any post:
```yaml
tags: [bioinformatics, python]
```

Tags don't generate pages automatically in Jekyll — that requires either a plugin (not supported on GitHub Pages without workarounds) or manually created tag pages. The practical approach for GitHub Pages is:
- Add tags to all post front matter
- Create a `/tags/` page that lists all tags and their posts (one page, anchor links per tag)
- Link tag badges on each post to the relevant anchor on `/tags/`

### Proposed Tag Set
| Tag | Covers |
|---|---|
| `bioinformatics` | DNA, RNA, protein structure, Project Rosalind problems |
| `python` | Code solutions, language concepts, programming patterns |
| `baseball` | EBL, fantasy sports, MLB data |
| `software` | Web apps, databases, APIs, system design concepts |
| `problem-solving` | Algorithms, logic, puzzle-solving process |
| `technical-writing` | Writing craft, documentation, communication |

### Implementation Tasks
- [ ] Add tags to all existing `_posts/` front matter
- [ ] Create `tags.md` page with anchor-linked sections per tag
- [ ] Add tag display and links to post layout
- [ ] Add tag badges to post excerpts on the home/list page
- [ ] Update `CLAUDE.md` drafts guidelines to require tags in front matter

---

## Step 2: Reader Experience Ideas

See the six proposals below — each is a candidate for implementation once tags are in place.

### Idea 1: "Start Here" page with reader paths
Instead of dropping every visitor into a reverse-chronological post list, a **Start Here** page routes different readers to the content most relevant to them. The current intro post already identifies distinct audiences (hiring managers, technical writers, Rosalind solvers, curious learners). A dedicated page could make that explicit with curated "reading paths" for each type — 3–4 recommended articles to read in order.

**Why it works for non-technical readers:** They don't know where to begin. A curated path removes that friction immediately.
**Effort:** Low — one new page, no plugin required.

---

### Idea 2: Project/series pages
Group articles into named series with a visual index — **Project Rosalind**, **EBL Deep Dives**, etc. Each series page shows the articles in order, with a brief description of what the series covers and what a reader will understand by the end.

**Why it works for non-technical readers:** A series has a beginning and an end. It feels like something they can complete, not an overwhelming archive.
**Effort:** Medium — requires a new layout or collection, or can be done as simple curated pages.

---

### Idea 3: Key takeaway box at the top of every post
A visually distinct callout box near the top of each article: **"What you'll understand after reading this."** One or two sentences. Sets expectations, helps readers self-select, and gives skimmers something to land on.

**Why it works for non-technical readers:** Non-technical readers often bail early if they can't tell whether an article is for them. This solves that in 10 seconds.
**Effort:** Low — a CSS class + a convention in the post template.

---

### Idea 4: Estimated reading time
Display reading time ("4 min read") next to the date on every post. For a blog targeting sub-750-word articles, most posts will be under 4 minutes — that's a strong signal to casual readers that the investment is low.

**Why it works for non-technical readers:** Removes a common reason to skip ("I don't have time for a long technical article").
**Effort:** Low — can be calculated with a simple Liquid snippet based on word count.

---

### Idea 5: Visual hero image or diagram per post
Each post gets a header image or custom diagram — not stock photography, but a simple illustration that captures the core concept visually. This connects directly to the visual-first approach already built into the article pipeline (the `<!-- VISUAL OPPORTUNITY -->` convention). The diagrams created for articles become the hero images.

**Why it works for non-technical readers:** Images are the first thing a reader sees when a link is shared on social media or in a message. A clear, interesting visual drives clicks and sets the tone before a word is read.
**Effort:** Medium — requires creating visuals for new posts; existing posts can be backfilled over time. Also requires adding `og:image` meta tags for social sharing.

---

### Idea 6: Related articles at the end of each post
After the last paragraph, surface 2–3 articles from the same tag(s). Keeps readers on the site, helps them discover content they didn't know existed, and reinforces the tag structure.

**Why it works for non-technical readers:** A reader who just understood one concept is primed to read another. Don't let them leave — give them a next step.
**Effort:** Medium — requires Liquid logic to find posts with matching tags, or can be done manually with a `related:` front matter field per post.

---

## Step 3: Modern Blogging Directions

Cutting-edge approaches worth considering as the blog grows.

### Digital Garden + Online Diary

#### What a digital garden is
A fundamental rethinking of what a blog is. Instead of reverse-chronological posts, a digital garden is a living set of interconnected notes that grow and link to each other over time — more like a personal wiki than a diary. Pages carry a maturity indicator (seedling / growing / evergreen) so readers know what's polished vs. rough. There's no "publish" event — you just tend the garden continuously.

**Key differences from a blog:**
| Blog | Digital Garden |
|---|---|
| Reverse-chronological | Organized by topic and connection |
| Posts are finished and static | Pages are always evolving |
| Reader follows the author's timeline | Reader follows their own curiosity |
| "Published on" date matters | Last-updated date matters more |
| One path through content | Many paths, linked by idea |

#### What this would look like for this site
The existing content already has strong concept threads running through many posts — graph theory, FASTA format, problem-solving approaches, Python patterns — that appear repeatedly but aren't connected to each other. A garden surfaces those connections explicitly.

**Concept hub pages** (living pages that grow over time):
- **Graph Theory** — linked to from grph, rear, sort, tree, and others; explains the concept once, deeply
- **FASTA Format** — referenced across a dozen bioinformatics posts
- **Python: Iterators vs. Generators** — a recurring Python concept worth its own page
- **Problem-Solving Approaches** — unrecognized assumptions, restating problems, when to look at others' solutions
- **The EBL Auction** — a hub for all EBL auction-related articles
- **Real-time Web** — connects SSE, live stats pipeline, concurrent bidding articles

A reader who lands on the graph theory hub sees every article that touches it, with a short annotation for each. They follow their curiosity, not the publication calendar.

#### The diary section
A diary is the *complement* to the garden, not a replacement for chronology. Where the garden organizes by idea, the diary captures the personal, time-stamped thread — what you're working on, what surprised you, what you got wrong, what you're thinking about next.

The closing thoughts in the "Sorting by Reversals" post ("I didn't have a single original thought that moved me forward...") are already diary writing. So is the personal aside in the Overlap Graphs post about having no memory of solving it in 2018. A diary section makes a deliberate home for that voice instead of burying it in problem-solving posts.

**What diary entries could look like:**
- Short (200–400 words), unpolished, dated
- What I worked on this week and what I learned
- A problem I'm stuck on and how I'm thinking about it
- A project update that doesn't fit a full article
- A reflection on something I published

The diary is also low-pressure content — it doesn't need the grammar checklist, the 750-word ceiling, or a defined thesis. It just needs to be honest.

#### Can this work in Jekyll and GitHub Pages?

**Partially.** Jekyll can approximate a garden:
- Multiple collections (`_notes/`, `_diary/`) configured in `_config.yml`
- Hub pages built as regular markdown pages
- Manual cross-linking between posts and hubs
- Tags already planned connect posts to concepts

**What Jekyll cannot do easily:**
- **Bidirectional links** — automatically showing "pages that link here" (backlinks) requires a plugin not available on GitHub Pages, or a custom JavaScript solution
- **Graph visualization** — the visual node-link map many gardens feature isn't supported natively
- **Wiki-style `[[page name]]` links** — requires a plugin; Jekyll uses standard markdown links only

**The honest answer:** Jekyll gets you 70% of a garden with manual effort. The remaining 30% — backlinks, graph view, wiki links — requires either workarounds or a different tool.

#### Better tools for a full garden

**Quartz (recommended if switching)**
Open source, free, deploys to GitHub Pages via GitHub Actions. Built specifically for digital gardens. Supports bidirectional backlinks, interactive graph view, full-text search, and wiki-style `[[links]]`. Accepts standard markdown with front matter — migration from Jekyll is mostly copying `.md` files. This is the strongest option for a full garden experience without leaving GitHub.

**Obsidian Publish**
$8/month. Best-in-class UI, native integration with Obsidian for writing, bidirectional links, graph view. The easiest path if already writing in Obsidian. Costs money; content lives on Obsidian's servers rather than your repo.

**Foam (VS Code + GitHub Pages)**
Free VS Code extension that adds wiki-links and backlinks to a GitHub Pages site. Less polished than Quartz but stays entirely in the existing GitHub workflow.

#### Recommendation
Start with Jekyll + the garden conventions (hub pages, manual cross-links, diary collection) to validate whether the structure works for this content. If backlinks and the graph view feel essential after living with it, migrate to Quartz — the markdown files transfer directly with minimal reformatting.

---

### Progressive Disclosure / Layered Articles
A single article has multiple depth levels — a 2-sentence summary, a 5-minute read, and a deep dive, all in one page. The reader chooses how far they go via accordions, "expand" sections, or simply clear visual breaks. Directly addresses the non-technical reader problem of "is this for me?"

**Why it fits:** The current articles explain technical concepts at one depth. Layering would let a casual reader get the idea and stop, while someone who wants to go deeper can keep reading.
**Effort:** Low to medium — mostly a writing and formatting convention; no new infrastructure required.

---

### Embedded Interactive Visuals
Tools like Observable, Svelte components, or simple JavaScript embeds let you put live, interactive charts directly in a post — sliders, toggleable parameters, animated diagrams the reader can control. The reader isn't just looking at a static chart; they're playing with it.

**Why it fits:** The visual-first pipeline already built into this blog (`<!-- VISUAL OPPORTUNITY -->`) is a natural lead-in. EBL budget math, bioinformatics sequence diagrams, and algorithm visualizations are all strong candidates. Nicky Case's *Explorable Explanations* (ncase.me) is the benchmark for this approach.
**Effort:** Medium to high — requires learning a tool (Observable is lowest barrier) and embedding output in Jekyll posts.

---

### Newsletter as Primary Channel
The email list becomes the publication; the website becomes the searchable archive. Readers subscribe and get content pushed to them rather than having to remember to visit. Tools: Ghost (self-hosted, built-in newsletter), Buttondown (simple, dev-friendly), or Substack (largest built-in audience). Most writers report 80–90%+ of reads happen via email once a list is established.

**Why it fits:** Short, non-technical articles about interesting topics are exactly what people read in email. Low commitment, high value.
**Effort:** Low to set up; ongoing commitment to send consistently.

---

### Audio Versions of Every Post
Auto-generate a podcast-quality audio version of each article and embed a player at the top. Tools like ElevenLabs or Podcastle produce natural-sounding narration from text. Widens the audience to commuters, people who prefer listening, and accessibility use cases.

**Why it fits:** Sub-750-word articles are short listens — under 5 minutes each. Easy to say yes to.
**Effort:** Low per article once a workflow is set up; requires embedding an audio player in the post layout.

---

### AI-Powered Semantic Search
Instead of a keyword search box, readers type a plain-English question and get the most relevant article. Uses text embeddings (via OpenAI, Anthropic, or similar) to match meaning rather than exact words. Increasingly easy to add as a static-site feature.

**Why it fits:** Once the EBL articles are published alongside the bioinformatics content, a reader asking "how does the auction work?" should find the right post even if it's titled something oblique.
**Effort:** Medium — requires an embedding pipeline and a search UI; several open-source static-site search tools now support this.

---

### Changelog and /now Page
Two simple transparency conventions gaining traction:
- **/now page**: What the author is focused on this month — current projects, what they're learning, what's coming. Updated monthly. Gives returning readers a reason to check back.
- **/changelog**: A running log of what articles were updated, what was corrected, and why. Builds trust with readers who notice when things change.

**Why it fits:** The blog already has a clear project arc (Rosalind → EBL → next project). A /now page makes that progression visible and gives the blog a sense of active life even between article bursts.
**Effort:** Very low — two static pages, updated manually.
