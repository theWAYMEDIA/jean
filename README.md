# jeanduplessis.net

Personal site of Jean Prieur du Plessis — business card, About, photo album and posts.
Plain Hugo, no theme: four layouts and one stylesheet.

```bash
hugo server -D      # local preview
hugo --minify       # production build -> public/
```

Push to `main` deploys to GitHub Pages.

## Adding a post

Make a folder `content/posts/<short-name>/` (or run `hugo new posts/<short-name>/index.md`)
with an `index.md` and the photos beside it:

```markdown
---
title: "My story"
date: 2026-10-26
---
Text here. An empty line starts a new paragraph.

![Optional caption](my-photo.jpg)
```

That is all a post needs. The post URL comes from the title, and the first photo in the
folder becomes the cover on the Posts page (set `cover: file.jpg` to choose another).

For a photo album at the end of a post, list the photos in front matter (see `memories/index.md`):

```yaml
gallery:
  - src: photo.jpg
    caption: "Optional caption"
```

Hugo resizes every photo to WebP at build time, so upload originals as they are.

Content was migrated from the WordPress site on 2026-10-26; post URLs are unchanged, and the old book pages (`static/<slug>/`) redirect to wayism.net.
