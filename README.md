# Repolex Knowledge Graph of google-deepmind/grid-cells

RDF knowledge graph data for [google-deepmind/grid-cells](https://github.com/google-deepmind/grid-cells), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/grid-cells
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d1a2304d9a54e5ead676af577a38d4d87aa73041
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d1a2304d9a54e5ead676af577a38d4d87aa73041
│           └── chunk-001.nq.gz
├── blob
│   ├── 06e9c6e8f3b32d5fce4a6ffd5f5ba0432f62a59c.nq.gz
│   ├── 0c7f0e52b0de9771aa86030b7c27797770313b26.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2f393ea1327fbde743b8075619657e668dfadf64.nq.gz
│   ├── 329f58a519c9b7abaffd5cd5031e04474a28f2ea.nq.gz
│   ├── 33526480765fab5e4a69f6662d6bdb96eefacb0f.nq.gz
│   ├── 8494e6046f764dc93d6f0c2b2fe832910b9a9900.nq.gz
│   ├── b725015e05887af933a0e915958525ec862955bf.nq.gz
│   └── db177d4ac70f76c2172ce65ca33c830d6cbd3ac5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d1a2304d9a54e5ead676af577a38d4d87aa73041.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 17 files
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

[google-deepmind/grid-cells](https://github.com/google-deepmind/grid-cells)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
