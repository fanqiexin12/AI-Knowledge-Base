# Conventions

Additional formatting and style guidelines for wiki pages.

## Writing Style

- Use clear, concise language
- Prefer active voice
- Include citations for all claims
- Flag uncertainties: "may be", "appears to", "unclear whether"

## Frontmatter Fields

```yaml
---
title: Required
type: Required (entity|concept|source|synthesis|overview)
tags: Optional array
created: YYYY-MM-DD (auto)
updated: YYYY-MM-DD (auto)
sources: Optional array of source file paths
related: Optional array of internal links
---
```

## Internal Linking

- Use Obsidian `[[page-name]]` syntax
- Link to categories explicitly: `[[entities/person]]`, `[[concepts/idea]]`
- Always link related pages at bottom of each document

## Source Citations

```markdown
- [Author, Year](raw/sources/document.pdf)
- [Article Title](raw/sources/article.md)
```

## Updating Pages

When updating a page with new information:
1. Update the `updated` frontmatter date
2. Note what changed in the log entry
3. If contradicting existing info, add a "## Contradictions" section
