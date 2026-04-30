# Medium Import — Agent Instructions

This repo produces Medium-importable HTML files. The primary use cases are:
1. **Write** a researched blog post as an HTML file ready to import into Medium.
2. **Backdate** a post to a specific historical date using Medium's `article:published_time` mechanism.

## How Backdating Works

Medium respects the `<meta property="article:published_time">` tag in imported HTML. Set it to any past UTC datetime to backdate the post. After import, Medium displays "Originally published at *** on [date]" at the bottom of the article.

See [backdate.html](./backdate.html) for the canonical template.

## Required HTML Structure

Every post file must follow this exact structure for Medium to parse it correctly:

```html
<!DOCTYPE html>
<html>
<head>
    <meta property="article:published_time" content="YYYY-MM-DDTHH:MM:SS.000Z" />
</head>
<body>
    <main>
        <article>
            <section>
                <div class="pw-post-title">
                    <h1>Your Post Title</h1>
                </div>
                <p class="pw-post-body-paragraph">Paragraph text...</p>
                <!-- more pw-post-body-paragraph paragraphs -->
            </section>
        </article>
    </main>
</body>
</html>
```

Key rules:
- Title must be in `<div class="pw-post-title"><h1>…</h1></div>`
- Every body paragraph must use `<p class="pw-post-body-paragraph">…</p>`
- `article:published_time` must be a valid ISO 8601 UTC timestamp
- Subheadings use `<h2>` or `<h3>` inside `<section>` (no wrapper class needed)
- Hyperlinks use standard `<a href="…">` tags inside paragraphs
- Images use `<figure><img src="…" alt="…"><figcaption>…</figcaption></figure>`

## Workflow

1. Research the topic using web search — gather facts, stats, and references.
2. Write the post in the HTML format above.
3. Name the output file descriptively, e.g., `my-post-title.html`.
4. Set `article:published_time` to the desired date (past date for backdating, today for current).

## Conventions

- One HTML file per post — no build step, no dependencies.
- Filename should be kebab-case matching the post title.
- All timestamps in UTC (`Z` suffix).
- Keep paragraphs concise (2–4 sentences) for Medium's reading experience.
- Include at least one external link in every post.
