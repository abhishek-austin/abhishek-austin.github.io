# ANB Solutions GitHub Pages Site

Static website for [abhishek-austin.github.io](https://abhishek-austin.github.io/).

The home page is a hand-built single page; the **Writing** section is a Jekyll
blog that GitHub Pages builds automatically.

## Publishing a blog post

See **[PUBLISHING.md](PUBLISHING.md)** — a step-by-step, no-tooling guide for
adding a weekly post through the GitHub web UI. Short version: add one Markdown
file to `_posts/` and commit.

## Local Preview

The home page alone (no blog build):

```sh
python3 -m http.server 8000 --bind 127.0.0.1   # then open http://127.0.0.1:8000/
```

The full site including the blog (matches what GitHub Pages publishes):

```sh
bundle install
bundle exec jekyll serve   # then open http://127.0.0.1:4000/
```

## Deploy

This repository is deployed by GitHub Pages, which builds the Jekyll site and
publishes it. Pushing to the configured Pages branch triggers a rebuild.

## Structure

- `index.html` - Hand-built single-page home (inline styles/JS). No Jekyll front
  matter, so it is published as-is.
- `blog/index.html` - The Writing index that lists all posts.
- `_posts/` - One Markdown file per post (`YYYY-MM-DD-title.md`).
- `_layouts/`, `_includes/` - Shared page shell, nav, and footer for the blog.
- `assets/css/site.css` - Blog styles (mirrors the home page design system).
- `post-template.md` - Copy this to start a new post.
- `_config.yml` - Jekyll configuration.
- `images/` - Web-ready image assets.

## Notes

- Keep committed images web-sized and stripped of personal camera metadata.
- Check the page locally before pushing, since pushes can trigger deployment.
- `index.html` keeps its own inline styles; the blog's `assets/css/site.css`
  intentionally mirrors that design system. Update both if the brand changes.
