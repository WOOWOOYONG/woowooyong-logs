# My Dev Site

Personal notes, projects, and short-form logs built with Astro 6, Tailwind CSS,
and TypeScript, then deployed as a static site on Cloudflare.

## Content

All content lives in this repository:

```text
src/content/
├── notes/       # Long-form articles
├── projects/    # Portfolio entries
└── logs/        # Short-form logs
```

To publish a log, add a Markdown file to `src/content/logs/` using the existing
frontmatter format, preview it locally, then commit and push the change. The
deployment rebuilds the site from the content in the same Git commit.

```md
---
pubDate: 2026-07-12T21:30:00+08:00
tags:
  - astro
---

Log content goes here.
```

## Commands

| Command             | Action                                           |
| :------------------ | :----------------------------------------------- |
| `pnpm install`      | Install dependencies                             |
| `pnpm dev`          | Start the development server at `localhost:4321` |
| `pnpm check`        | Run Astro and TypeScript checks                  |
| `pnpm lint`         | Run ESLint                                       |
| `pnpm format:check` | Check formatting                                 |
| `pnpm build`        | Check and build the production site to `dist/`   |
| `pnpm preview`      | Preview the production build                     |

Production builds require `SITE_URL` or `CF_PAGES_URL` to contain the deployed
site URL.
