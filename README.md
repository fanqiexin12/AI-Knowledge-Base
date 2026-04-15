# LLM Knowledge Base

**Live Wiki**: https://fanqiexin12.github.io/AI-Knowledge-Base/

A personal knowledge base built using the [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) by Andrej Karpathy.

## Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    Three Layers                         │
├─────────────────────────────────────────────────────────┤
│  raw/          │ Immutable sources (articles, papers)   │
│  wiki/         │ LLM-generated markdown (synthesized)   │
│  schema/       │ Conventions & instructions for LLM    │
└─────────────────────────────────────────────────────────┘
```

## Quick Start

1. **Add sources**: Place documents in `raw/sources/`
2. **Ingest**: Ask LLM to "ingest the new source"
3. **Query**: Ask questions about your wiki
4. **Lint**: Periodically ask LLM to "lint the wiki"

## Key Files

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Schema — tells LLM how to maintain the wiki |
| `wiki/index.md` | Catalog of all wiki pages |
| `wiki/log.md` | Chronological record of operations |

## Why This Works

> "The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping. LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass."

## Tools

- **Obsidian** — recommended IDE for browsing/managing the wiki
- **Obsidian Web Clipper** — browser extension to clip articles as markdown
- **qmd** — local search engine for markdown (optional, as wiki grows)

## Credits

Pattern from [Karpathy's LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
