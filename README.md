# Repolex Knowledge Graph of skypilot-org/new-cloud-skeleton

RDF knowledge graph data for [skypilot-org/new-cloud-skeleton](https://github.com/skypilot-org/new-cloud-skeleton), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download skypilot-org/new-cloud-skeleton
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 94409beacc6a934840076399f5f01a9059945663
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 94409beacc6a934840076399f5f01a9059945663
│           └── chunk-001.nq.gz
├── blob
│   ├── 0327ed31c82a4b872257854e1ecbb0c53a9a8e2c.nq.gz
│   ├── 158b09a82ed9b3270f1e9b99ef192acd66b44d30.nq.gz
│   ├── 25da13fb911655a3ce9f439d9c5b983547fdf6a0.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 35122b7910cf07e2f002acfce094a75dc52bf646.nq.gz
│   ├── 3694a597333da6809f11485e516576747583fd51.nq.gz
│   ├── 584b9607636df0fe92ea5bf303ab4edda5ec202d.nq.gz
│   ├── 5e53478422d0ab72cf8ccf4d1c1dff51ab379aea.nq.gz
│   ├── 601e981466d41543b1f652d54d49b5fe27c4a3c7.nq.gz
│   ├── 68bc17f9ff2104a9d7b6777058bb4c343ca72609.nq.gz
│   ├── 6f0bc29b02cc962c74642b6746e8fc34ce9c4e64.nq.gz
│   ├── 7ef4d479e54b782b56f368ce3889016719e3bd4b.nq.gz
│   ├── 9906642066be74bbbbc293dda4aa442e3987732f.nq.gz
│   ├── 9c0708decc5d6d1040c296e86b8e8cedf8aa0a48.nq.gz
│   ├── baa152f1395ccc1e0a22e37dd7738980c7c6289c.nq.gz
│   ├── c805eeb72ef7d6654e45ffe826d97957e377d04a.nq.gz
│   ├── cbfb7b65821835e778d91be2899ab6b1f1f1a374.nq.gz
│   └── e2b1756e857a92f63267e5dadbe2c1da9cd39b9b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 94409beacc6a934840076399f5f01a9059945663.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 25 files
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
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[skypilot-org/new-cloud-skeleton](https://github.com/skypilot-org/new-cloud-skeleton)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
