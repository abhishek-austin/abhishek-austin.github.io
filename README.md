# ANB Solutions GitHub Pages Site

Static website for [abhishek-austin.github.io](https://abhishek-austin.github.io/).

## Local Preview

Run the site from the repo root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open <http://127.0.0.1:8000/>.

## Deploy

This repository is deployed by GitHub Pages. Pushing to the configured Pages branch publishes the latest committed files.

## Structure

- `index.html` - Single-page site with inline styles and JavaScript.
- `images/` - Web-ready image assets used by the page.

## Notes

- Keep committed images web-sized and stripped of personal camera metadata.
- Check the page locally before pushing, since pushes can trigger deployment.
