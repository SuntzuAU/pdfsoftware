# Build Rules - Architecture, Deployment, Images

## Why Astro

Astro is non-negotiable. Landing page performance is the primary SEO lever. Static HTML by default, zero client-side JS unless explicitly added. Fast Core Web Vitals directly improve Google ranking. Never introduce React, Vue, or any client-side framework for content pages.

## Architecture Pattern

Reference: `dragonprofessional16.com.au`:
- Single self-contained `index.astro` - no separate Nav component that imports pages for CSS variables
- All content driven from `src/site.config.json`
- Product subpages use `[product].astro` dynamic route
- Images served from Cloudflare R2 via `PUBLIC_R2_BASE` env var
- Blog posts in `src/content/news/` with required frontmatter

## Content Collection Standard

- Folder: `src/content/news/` | Collection name: `news` | Routes: `src/pages/news/`
- Do NOT create or use a `blog` collection or `src/content/blog/` folder

## CSS Rules

- Never use `var(--primary)` or `var(--accent)` for background-color on dark sections in `[product].astro`
- Extract colours in frontmatter as JS variables, apply via inline style

## Performance

- Minimise JS - defer, lazy load, or eliminate
- Video embeds: thumbnail facade, load iframe on click only
- Images except hero: `loading="lazy"` `decoding="async"` | Hero: `loading="eager"`
- System fonts where possible | Mobile first: 375px minimum

## Deployment

- Cloudflare Pages | Both apex AND www as custom domains
- `PUBLIC_R2_BASE`: `https://pub-c7a09e1ddb7c45e6a38fcdca1e4b6897.r2.dev` (set in GitHub Actions AND Cloudflare Pages)
- Touch `src/site.config.json` to force full rebuild

## Image Generation - NEVER Autonomous

Every blog post: 3 images (heroImage, breakImage1, breakImage2 + alt text for each).

1. Draft article, get owner approval
2. Prepare 3 image prompts, show owner
3. Wait for owner to say "go"
4. Call Worker via Chrome MCP
5. Commit article + images together

```
POST https://master-image-generator.speech-recognition-cloud.workers.dev/generate
Body: { "prompt": "...", "name": "seo-slug-here" }
```

SEO naming: slug-first, e.g. `dragon-medical-one-australia-gp-dictation-hero`

If Chrome MCP unavailable: inform owner, wait. Do NOT commit without images.

## Technical Gotchas

- No emoji/Unicode in site.config.json - GitHub API corrupts it
- YAML frontmatter: spaces after colons
- push_files cannot modify .github/workflows/ - provide for manual paste
- Cloudflare 301 redirects cached aggressively - test in incognito
