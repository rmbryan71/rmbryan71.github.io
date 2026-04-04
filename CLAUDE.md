# Claude Guidelines — rmbryan71.github.io

## Blog Context
This is a Jekyll blog hosted on GitHub Pages at robertbryan.net. The author writes short articles about personal projects — technical topics made accessible to a general audience.

## Audience
Non-technical readers. Assume no prior knowledge of programming, biology, data science, or any specialized field. A curious, intelligent person who has never written code or studied the subject should be able to read and understand every article.

## Voice & Tone
- Conversational and direct — write like you're explaining something to a smart friend
- First person is fine
- Avoid jargon; when a technical term must be used, always define it immediately in plain language
- No unnecessary filler phrases ("it's worth noting that", "in conclusion", etc.)

## Article Length
**Hard limit: 750 words.** Always track word count when drafting or editing. If content exceeds 750 words, cut rather than summarize — tighter is better.

## Visual Opportunities
Actively look for opportunities to suggest graphics, charts, and diagrams that could replace or supplement text explanations. When a concept involves a process, relationship, comparison, or data, flag it with a `<!-- VISUAL OPPORTUNITY: [description] -->` comment. Prefer visuals over long prose for technical concepts.

## Article Pipeline
Content moves through these stages — each folder has its own CLAUDE.md with stage-specific rules:

1. `_ideas/` — raw ideas, questions, project notes
2. `_outlines/` — structured outlines with sections and key points
3. `_drafts/` — full prose drafts, grammar-checked, ready to polish
4. `_posts/` — published articles (Jekyll format with front matter)

## Jekyll Notes
- Published posts live in `_posts/` and follow the filename format `YYYY-MM-DD-slug.md`
- Front matter is required: `layout`, `title`, `date`, `categories`, and optionally `excerpt`
- The excerpt separator is `<!--break-->`
