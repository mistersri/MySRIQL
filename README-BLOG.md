# Blog — quick reference

The blog lives at **mistersri.com/blog**. It's powered by Jekyll, which GitHub Pages builds for you automatically on every push.

## File layout

```
_config.yml           Jekyll config — rarely needs changes
Gemfile               Ruby deps for local preview only

_layouts/
  post.html           Layout for an individual post page (e.g. /blog/2026/05/25/hello/)

_posts/               Published posts. Filenames MUST be YYYY-MM-DD-slug.md
  2026-05-25-hello-world.md

_drafts/              Unpublished posts. No date in filename. Not deployed.
  example-draft.md

blog/
  index.html          The /blog/ page itself (TOC + all posts inline)

images/blog/          Drop blog images here, reference as /images/blog/foo.jpg
```

## Writing a new post (the fast path)

1. Create a file in `_drafts/`. Any filename — e.g. `_drafts/my-new-idea.md`.
2. Start the file with frontmatter:

   ```
   ---
   title: "Whatever the post is called"
   description: A one-sentence summary for SEO and social previews.
   ---
   ```

3. Write markdown below the frontmatter.
4. Preview locally (see below). Iterate.
5. When ready to publish:
   - Rename and move the file to `_posts/YYYY-MM-DD-slug.md`
   - Add `date: 2026-05-25` to the frontmatter (or just rely on the filename date)
   - `git push`. GitHub Pages rebuilds in ~1 minute.

## Previewing locally

You need Ruby installed (macOS ships with it; on Linux/Windows, install Ruby 3.x).

One-time setup, from the repo root:

```
gem install bundler
bundle install
```

Then anytime you want to preview:

```
bundle exec jekyll serve --drafts --livereload
```

Open http://localhost:4000/blog/ — the page reloads automatically when you save changes. Add `--drafts` to include drafts, omit it to see exactly what the public site shows.

## Including images

Drop the image file into `/images/blog/`, then in your markdown:

```markdown
![A short alt description](/images/blog/your-image.jpg)
```

For a caption, use HTML inside the markdown:

```html
<figure>
  <img src="/images/blog/your-image.jpg" alt="Short alt description">
  <figcaption>Caption text here.</figcaption>
</figure>
```

## Frontmatter reference

```yaml
---
title: "Post title"           # required
date: 2026-05-25              # optional — defaults to date in filename
description: One sentence.    # optional but recommended for SEO
---
```

## What URLs each post gets

- The post appears inline on `/blog/` (the single-page archive with TOC).
- It also gets its own page at `/blog/YYYY/MM/DD/slug/` for shareable permalinks and better SEO.
- In the TOC, clicking a title scrolls down to the post on the same page.
- Clicking the post title itself jumps to that post's dedicated URL.

## What's NOT touched

Your existing `index.html`, `/css`, `/images` (other contents), favicons, `CNAME`, and `404.html` keep working exactly as they did. Jekyll only processes files with frontmatter or in `_*` folders — everything else passes through unchanged.

## Adding a link from the homepage

Your `index.html` doesn't currently link to the blog. To add one, you might insert this just below the bio paragraph or near the LinkedIn icon (matching your existing style):

```html
<a href="/blog/" style="color: #aaa; font-size: 0.95rem; letter-spacing: 0.04em;">writing →</a>
```

But that's a separate edit — I left your index.html alone.
