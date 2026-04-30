---
description: "Research a topic and write a complete Medium blog post as an importable HTML file"
name: "Write Medium Post"
argument-hint: "Topic or title for the blog post"
agent: "agent"
tools: ["fetch_webpage", "create_file", "file_search"]
---

Research the topic provided by the user and write a complete Medium blog post, saved as an HTML file ready to import into Medium.

## Steps

1. **Research** — Use web search / fetch to gather:
   - Key facts, statistics, and recent developments on the topic
   - 2–3 authoritative sources to cite or link within the post
   - A compelling angle or unique insight for the post

2. **Outline** — Plan the structure:
   - Hook opening paragraph
   - 3–5 main sections with subheadings
   - Actionable takeaway or conclusion

3. **Write** — Produce the post following the HTML structure in [AGENTS.md](../AGENTS.md):
   - Use `<div class="pw-post-title"><h1>…</h1></div>` for the title
   - Use `<p class="pw-post-body-paragraph">…</p>` for every body paragraph
   - Use `<h2>` for section headings inside `<section>`
   - Link sources inline with `<a href="…">anchor text</a>`
   - Set `article:published_time` to today's date in UTC (or the date the user specifies)

4. **Save** — Create the file as `<kebab-case-title>.html` in the workspace root.

## Quality Checklist

- [ ] Opening paragraph hooks the reader without giving everything away
- [ ] Every factual claim has an inline link to the source
- [ ] Post is 600–1500 words (typical Medium sweet spot)
- [ ] Conclusion includes a clear takeaway or call to action
- [ ] HTML validates against the structure in AGENTS.md
