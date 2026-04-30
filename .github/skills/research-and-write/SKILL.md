---
name: research-and-write
description: "Research a topic with web sources and write a complete Medium blog post as an importable HTML file. Use when: write a blog post, research and write, draft a Medium article, create a post about, write about a topic, new post on. Produces a timestamped HTML file + a sources log."
argument-hint: "Topic or working title for the post"
---

# Research-and-Write

Researches a topic online and produces two files:
1. `<kebab-title>.html` — Medium-importable post (follows [AGENTS.md](../../../AGENTS.md))
2. `sources/<kebab-title>.md` — Source log for fact-checking and future editing

## Procedure

### Step 1 — Scope the post
- Confirm the topic and desired angle with the user if ambiguous.
- Decide target length: **short** (~600 words, 3 sections), **standard** (~1000 words, 5 sections), **long** (~1500 words, 7 sections). Default: standard.
- Ask for a target publish date if the user wants backdating; otherwise default to today.

### Step 2 — Research
Fetch at least **4 sources**. Aim for:
- 1–2 primary sources (official docs, studies, gov/org data)
- 1–2 reputable secondary sources (major news, well-known blogs)
- 1 "surprising angle" source (counter-argument, niche insight, or stat that reframes the topic)

Record every source in [sources template](./assets/sources-template.md) format while researching — do not wait until after writing.

### Step 3 — Outline
Draft the structure before writing prose:
```
Title
Hook paragraph (1–2 sentences)
Section 1: <heading>
Section 2: <heading>
...
Conclusion / CTA
```
Show the outline to the user and proceed unless they ask for changes.

### Step 4 — Write
Use [post-template.html](./assets/post-template.html) as the starting point.

Rules:
- Every `<p>` must have `class="pw-post-body-paragraph"`
- Section headings → `<h2>` (no wrapper class)
- Inline links → `<a href="URL">anchor text</a>` inside `<p>` tags
- Keep paragraphs 2–4 sentences
- Do NOT use `<ul>/<ol>` — Medium strips list formatting on import; convert lists to prose or use em-dash run-ons
- Set `article:published_time` to the target date at noon UTC: `YYYY-MM-DDT12:00:00.000Z`

### Step 5 — Save both files
- Post → `<kebab-title>.html` at workspace root
- Sources → `sources/<kebab-title>.md`

### Step 6 — Quality check (self-review before finishing)
- [ ] Every factual claim has an inline link to a researched source
- [ ] `article:published_time` is a valid ISO 8601 UTC timestamp
- [ ] File uses only allowed HTML elements (no `<ul>`, `<ol>`, `<div>` in body)
- [ ] Opening hook does not start with "In this post…" or "Today we'll…"
- [ ] Conclusion has a clear takeaway or call to action
- [ ] Sources file lists all fetched URLs with title, date, and key fact used

## Output Summary
Tell the user:
- File paths created
- Publish date embedded
- Number of sources logged
- Word count (approximate)
