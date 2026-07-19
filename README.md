# Woodside

Woodside is a minimal, contemplative theme for [Ghost](https://github.com/TryGhost/Ghost), based on [TryGhost/Zap](https://github.com/TryGhost/Zap) and [Tufte CSS](https://github.com/edwardtufte/tufte-css/blob/gh-pages/tufte.css).

**Demo: https://alecstewart.com**

# Instructions

1. [Download this theme](https://github.com/stewalec/woodside/archive/main.zip)
2. Log into Ghost, and go to the `Design` settings area to upload the zip file

# Development

Woodside is intentionally small. You can edit the Handlebars templates in the theme root and the stylesheet in `/assets/screen.css`.

From the theme's root directory:

```bash
# Enable the package manager pinned in package.json
corepack enable

# Install dependencies
pnpm install

# Check theme compatibility
pnpm test
```

# Routes

Here is a custom `routes.yaml` file that works well with this theme:

```yaml
routes:
  /: home

collections:
  /thinking/:
    permalink: /thinking/{slug}/
    filter: tag:hash-thinking
    template: thinking
  /writing/:
    permalink: /writing/{slug}/
    filter: tag:hash-writing
    template: writing

taxonomies:
  tag: /{slug}/
  author: /author/{slug}/
```

# TODO

- [ ] Comments UI styling
- [ ] Tag page
- [ ] Author page
- [ ] Subscribe

# Contribution

If you're looking to contribute or raise an issue, head over to the [stewalec/woodside](https://github.com/stewalec/woodside) repository.

# Copyright & License

Copyright (c) 2013-2026 Ghost Foundation - Released under the MIT license.
