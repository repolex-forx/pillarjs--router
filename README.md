# Repolex Knowledge Graph of pillarjs/router

RDF knowledge graph data for [pillarjs/router](https://github.com/pillarjs/router), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download pillarjs/router
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e6d6b609fc355e558174ccd5b1db646f739fe88c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── e6d6b609fc355e558174ccd5b1db646f739fe88c.nq.gz
│   └── repolex
│       └── e6d6b609fc355e558174ccd5b1db646f739fe88c
│           └── chunk-001.nq.gz
├── blob
│   ├── 123eca28ee23642d490965db4fbfc28f7cb98d35.nq.gz
│   ├── 1887d7898ca101e3caa9128ab679a57065686be9.nq.gz
│   ├── 218fd5720f0dba9a507306325ff9e654a44918ce.nq.gz
│   ├── 237e1b67d3b34c1ea0b860e578694cae98fc7903.nq.gz
│   ├── 2fab2fbb949492af39475ed7e48cbf8e6e0cb2a2.nq.gz
│   ├── 4358aebddff7d665ae2012eb0ed4efaf95c2b2c8.nq.gz
│   ├── 6a4408ff3499e63fe95f77d50f11989a39cea860.nq.gz
│   ├── 8db59c3b3cdeeaec12711d83b78928d337a51bde.nq.gz
│   ├── 8eb4f63b01c9383d14fe2e49e52b7ca24964987e.nq.gz
│   ├── b292257a44b2de8d9d5ea67ed958d1bd9bf7ab9b.nq.gz
│   ├── b440e404ea19b94e27b0991e09b911b4f13605f3.nq.gz
│   ├── b4bcfac08298807660e8f05d0ec016f28ac25d82.nq.gz
│   ├── b62d4e16f4c8e13891c25bc2b2385cab9ee71abd.nq.gz
│   ├── c39cc4936a927374396d0e92c4f49908e3b3539c.nq.gz
│   ├── cdb36c1b4662559d2880d7a1ae9e65ca7497f47e.nq.gz
│   ├── cfedcac173f6a887bceab11d4022110453eed97a.nq.gz
│   ├── d23de00e03e74ac28fcdc9eb28d3fd21087e4136.nq.gz
│   ├── dd51298b945edb7887f6689a9db8bd5a37c47b6c.nq.gz
│   ├── e8fca8a685a30a89a8e9129a2668b08e0c713a92.nq.gz
│   ├── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
│   └── fe7019d464e04fcdac3789fc1526af3e289c7aae.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── e6d6b609fc355e558174ccd5b1db646f739fe88c.nq.gz
├── filetree
│   └── e6d6b609fc355e558174ccd5b1db646f739fe88c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 31 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |

## Source repository

[pillarjs/router](https://github.com/pillarjs/router)

---
*Parsed on 2026-09-16 by [repolex](https://repolex.ai)*
