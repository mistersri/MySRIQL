---
title: "Hello, world"
date: 2026-05-25
description: A welcome note and a quick tour of how this blog works.
---

This is the first post. It exists mostly to show how things look — feel free to delete it once you've written something real.

## A heading

Body paragraphs render in Cormorant Garamond at a comfortable reading size. Links look like [this one](https://mistersri.com) — underlined in terracotta, the same accent color as on the home page.

You can use **bold** sparingly, or *italics* when you want to lean on a word. Inline `code` is also styled.

## Lists

A short, unordered list:

- Climb something tall
- Read something old
- Write something honest

Or numbered, when order matters:

1. First do this
2. Then this
3. Then maybe rest

## Images

Drop images into `/images/blog/` and reference them with standard markdown:

```markdown
![A wide canyon at dawn](/images/blog/canyon.jpg)
```

You can also wrap them in a figure with a caption using HTML inside markdown:

```html
<figure>
  <img src="/images/blog/canyon.jpg" alt="A wide canyon at dawn">
  <figcaption>The view from somewhere worth getting to.</figcaption>
</figure>
```

## Blockquotes

> The best time to plant a tree was twenty years ago. The second best time is now.

## A code block

```python
def hello(name):
    return f"Hi, {name}."
```

---

That's the tour. Write your next post by adding a file to `_posts/` named `YYYY-MM-DD-your-slug.md` — or stash it in `_drafts/` first and preview locally until it's ready.
