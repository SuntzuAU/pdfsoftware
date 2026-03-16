# Interlink Rules - Cross-Site and Internal Linking

## Why This Matters

Each internal link builds page authority. Each cross-site link builds network effect across the domain portfolio. Every piece of content should benefit every site.

## Rules - Non-Negotiable

- **No footer links. Ever.** All links contextual in body copy.
- Every blog post: `internalLinks` and `externalLinks` in frontmatter
- Min 1 internal, max 3 | Min 1 external, max 2
- Never link same external site twice on one page
- Never repeat same anchor text to same destination across the site
- Links must feel natural - not bolted on

## Before Writing Content

1. Read `src/data/link-network.json` for anchor pools, bridge phrases, adjacency map, authority language
2. Read `src/data/link-usage.json` for coverage counts and anchors already used
3. Pick external target: lowest coverage count with relevant topic match
4. Select anchor from appropriate pool, check it hasn't been used

## Frontmatter Standard

```yaml
internalLinks:
  - to: "/news/related-post"
    anchor: "descriptive anchor text"
externalLinks:
  - to: "voicerecognition.com.au"
    anchor: "authorised Dragon reseller Australia"
    url: "https://www.voicerecognition.com.au"
context: "descriptive"  # medical, legal, descriptive, brand, action, comparison, generic
```

## The Productivity Bridge

All sites address the same problem: professionals spending too much time on documentation. Use the adjacency map in link-network.json for conclusion paragraphs. Dragon = input. PDF = output. Cloud printing = last mile.

## Draft Checklist

- [ ] Internal link with descriptive anchor
- [ ] Cross-site link (different target from previous post)
- [ ] Anchor text not already used for that destination
- [ ] Both links feel natural
- [ ] "Links used" summary at end of draft

```
LINKS USED IN THIS POST
Internal: [anchor] -> [URL]
Cross-site: [anchor] -> [domain]
```

Claude must suggest 2-3 anchor text options and let owner choose. Never commit without approval.
