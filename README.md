# Repolex Knowledge Graph of tusharsadhwani/pytokens

RDF knowledge graph data for [tusharsadhwani/pytokens](https://github.com/tusharsadhwani/pytokens), parsed by [repolex](https://repolex.ai).

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
rlex download tusharsadhwani/pytokens
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e087823ddf4ac81e048a0874fbdf7cdd856579ea
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e087823ddf4ac81e048a0874fbdf7cdd856579ea
│           └── chunk-001.nq.gz
├── blob
│   ├── 09162849465409b6dc78523e1dfba522ff29a832.nq.gz
│   ├── 2b6bc7d409e97af98518e26fdcb1e4133bad5b06.nq.gz
│   ├── 54d472e386ac79e7be0d94904b43a090d549882e.nq.gz
│   ├── 597f8d7802144b655620d44a60f39c19acbf8bdb.nq.gz
│   ├── 6ae31dc4d281ae51e5f5ac6995f607c86d9c3f91.nq.gz
│   ├── 6f9441f4656be00771ccd6c7518c66767df309cf.nq.gz
│   ├── 827ec4840e5817513d67dc7dc83a8dac36edc6e5.nq.gz
│   ├── 84824e73968bbd691fb485f05d40d4d60449bd68.nq.gz
│   ├── 8bbaa62ab16e95d93bf3c0a1bb43ea349aa73f7c.nq.gz
│   ├── 97cc5134c3bf46d7df3d59f66feade96a67a5671.nq.gz
│   ├── afbf37091411d59b986223ff623e55bf1cffa74e.nq.gz
│   ├── b8605e97df09a3d80c60628003954abdab13623e.nq.gz
│   ├── ce2d8c5f7c36a9ad7dca239f92a467825efb0f23.nq.gz
│   ├── d3245e747a8bc085800a555ac3ea9f4ccdafbe4b.nq.gz
│   ├── d771321a7bf9b461ae6fc137c1e5d53593f8ed9b.nq.gz
│   ├── def1a5ad7e10107456a048eb37339e8fb527d7f7.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── e8ad047ba00f7c4d754b060e5e84bf024bf6ea9e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e087823ddf4ac81e048a0874fbdf7cdd856579ea.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[tusharsadhwani/pytokens](https://github.com/tusharsadhwani/pytokens)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
