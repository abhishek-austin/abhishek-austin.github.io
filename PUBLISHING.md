# How to publish a weekly post

This site has a **Writing** section at <https://abhishek-austin.github.io/blog/>.
Each post is one text file. Publishing a post means adding one file and saving
it — GitHub does the rest, and the post is live in a minute or two.

No software to install. Everything below is done in the browser on github.com.

---

## The weekly workflow (5 minutes)

1. Go to the **`_posts`** folder in the repository:
   <https://github.com/abhishek-austin/abhishek-austin.github.io/tree/main/_posts>
2. Click **Add file → Create new file**.
3. Name the file using this exact pattern — **date first, then a short title**,
   ending in `.md`:

   ```
   2026-06-30-a-few-words-from-the-title.md
   ```

   - Use the date you want shown on the post (`YYYY-MM-DD`).
   - Use lowercase words separated by hyphens, no spaces.

4. Paste in the post. The easiest way: open **`post-template.md`** in the repo,
   copy everything, paste it into your new file, and replace the placeholders.
   The top section (between the `---` lines) is the post's settings:

   ```
   ---
   title: "The headline of the post"
   subtitle: "Optional one-line setup."
   date: 2026-06-30
   tags: [Leadership, AI]
   linkedin: https://www.linkedin.com/posts/...your-post-link...
   excerpt: "1–2 sentence summary used on the index and link previews."
   ---

   The body of the post goes here. Paste the LinkedIn text. Leave a blank
   line between paragraphs.
   ```

5. Scroll down, click **Commit changes**, then **Commit changes** again.

That's it. Within a couple of minutes the post appears at the top of the
[Writing page](https://abhishek-austin.github.io/blog/).

---

## Filling in the settings (the part between the `---` lines)

| Field      | Required? | What to put                                                        |
|------------|-----------|--------------------------------------------------------------------|
| `title`    | Yes       | The headline. Keep the quotation marks around it.                  |
| `date`     | Yes       | `YYYY-MM-DD`. Should match the date in the file name.              |
| `linkedin` | Strongly  | The link to the matching LinkedIn post. Adds a "Discuss on LinkedIn" button and connects the two. |
| `excerpt`  | Optional  | A 1–2 sentence summary. If left out, the first lines are used.     |
| `subtitle` | Optional  | A single setup line shown under the headline.                      |
| `tags`     | Optional  | A few topics in square brackets, e.g. `[AI, Scaling]`.            |

### Getting the LinkedIn link
On the LinkedIn post, click the **`...`** menu in the top-right of the post and
choose **Copy link to post**. Paste that into the `linkedin:` field. This is what
makes the website and LinkedIn point at each other.

---

## Writing the body (light formatting)

The body is plain text with a few optional touches:

- Blank line between paragraphs.
- `## Heading` for a section heading (two hash marks + a space).
- `**bold**` and `*italic*`.
- Lines starting with `- ` become bullet points.
- A line starting with `> ` becomes a pull quote.
- Links: `[text to show](https://the-url.com)`.

You can paste LinkedIn text directly and it will look right. The formatting above
is only if you want headings, bold, etc.

---

## Good to know

- **Posts are sorted by date automatically** — newest first. You don't arrange anything.
- **To fix a typo:** open the post file in `_posts`, click the pencil (✏️) icon,
  edit, and commit. Changes go live in a minute or two.
- **To unpublish a post:** open it, click the trash icon, and commit. (Or change
  its `date` to a future date and it won't show until then.)
- **The home page is a separate file** (`index.html`) and is not affected by
  anything in this workflow.

---

## For a developer / local preview (optional)

You don't need this to publish, but to preview locally:

```sh
bundle install
bundle exec jekyll serve
# open http://127.0.0.1:4000/blog/
```

The site is built by GitHub Pages with Jekyll. Posts live in `_posts/`, shared
look-and-feel lives in `_layouts/`, `_includes/`, and `assets/css/site.css`.
