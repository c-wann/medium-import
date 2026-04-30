---
description: "Generate a Medium-importable HTML file with a specific backdate for an existing post title or content"
name: "Backdate Medium Post"
argument-hint: "Post title and target date (e.g., 'My Post Title, 2022-03-15')"
agent: "agent"
tools: ["create_file", "read_file"]
---

Create a Medium-importable HTML file backdated to the date the user specifies.

## What the user should provide

- **Title** of the blog post
- **Target date** — any past date in any common format (e.g., "March 15, 2022", "2022-03-15", "15/03/2022")
- **Content** — optional; if omitted, produce a placeholder body with instructions on where to paste their content

## Steps

1. **Parse the date** — Convert the user's date to a UTC ISO 8601 timestamp:
   - Use noon UTC to avoid timezone edge cases: `YYYY-MM-DDT12:00:00.000Z`
   - Confirm the interpreted date with the user before writing the file

2. **Build the HTML** — Use this exact structure (see [backdate.html](../../backdate.html) for reference):

```html
<!DOCTYPE html>
<html>
<head>
    <meta property="article:published_time" content="YYYY-MM-DDT12:00:00.000Z" />
</head>
<body>
    <main>
        <article>
            <section>
                <div class="pw-post-title">
                    <h1>POST TITLE HERE</h1>
                </div>
                <p class="pw-post-body-paragraph">CONTENT HERE</p>
            </section>
        </article>
    </main>
</body>
</html>
```

3. **Save** — Write the file as `<kebab-case-title>.html` in the workspace root.

4. **Remind the user** how to import:
   - Go to medium.com → Stories → Import a story
   - Paste the path or upload the `.html` file
   - After import, verify "Originally published at … on [date]" appears at the bottom

## Notes

- The `article:published_time` value must be a **past** date; Medium ignores future timestamps.
- If the user provides content inline, format it with `<p class="pw-post-body-paragraph">` paragraphs.
- If content is a full draft, also apply subheadings using `<h2>` tags within the `<section>`.
