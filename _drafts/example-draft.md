---
title: "A draft you can preview but the world can't see"
description: This file lives in _drafts/ — it won't appear on mistersri.com until you move it to _posts/ and add a date to the filename.
---

This post is a draft. It will show up when you run:

```
bundle exec jekyll serve --drafts
```

…but it will **not** be deployed to the public site. Drafts let you write, save, and iterate as long as you want before committing to publish.

## Workflow

1. Create a file in `_drafts/` with any name — e.g. `_drafts/my-half-finished-idea.md`
2. Write whatever you want. No date in the filename needed yet.
3. Preview locally with `--drafts` to see how it'll look.
4. When you're ready to publish: rename and move the file to `_posts/YYYY-MM-DD-my-slug.md`, and set the `date:` in the frontmatter.
5. Commit and push. GitHub Pages rebuilds within a minute or two.

Delete or replace this file whenever you like.
