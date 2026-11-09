# Repolex Knowledge Graph of TopQuadrant/shacl-js

RDF knowledge graph data for [TopQuadrant/shacl-js](https://github.com/TopQuadrant/shacl-js), parsed by [repolex](https://repolex.ai).

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
rlex download TopQuadrant/shacl-js
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7ed360b795ab66cdb78c365fd136a82c524c0127
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7ed360b795ab66cdb78c365fd136a82c524c0127
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cf4afe385440cca2b215d5fb8d3806e8dc3dc28.nq.gz
│   ├── 0f846c757297b13fdf71955df823a36b3a1c3e07.nq.gz
│   ├── 12bbb2cb32f86a8b51cd7ce1f9f677c4e21d3d9c.nq.gz
│   ├── 24e6b2e75c9fc66c1330d38b60211b8d31120818.nq.gz
│   ├── 2a4561f7af57a88946a252c3c5fa1d250a462171.nq.gz
│   ├── 3cd59db2b0ff79098c9af6ed9079d26fdea8bc61.nq.gz
│   ├── 42df1921e8ff76d138b7645eeb47cf76774cb7f8.nq.gz
│   ├── 464a7e3532cfc9b26721a6f1487fa4e90c35a4db.nq.gz
│   ├── 4bd417ce8eda8afb126175cc69867635edc38fc0.nq.gz
│   ├── 661d9a863778315f5956ddfc7cf0b5ed418d329b.nq.gz
│   ├── 6c0dd50b57fb67ac71d659d5e650689db223cf69.nq.gz
│   ├── 78e18f595d0093c00885cc2f68dcae0ba7671c3d.nq.gz
│   ├── 7ce2be8cd42556fdc07bc5204fd0f4d30cba02a5.nq.gz
│   ├── 8dada3edaf50dbc082c9a125058f25def75e625a.nq.gz
│   ├── a03f0491b2ff9b50bc2d1559fea48ce711adfe2d.nq.gz
│   ├── b14535bb1e82abef5a4d72d059345d53fa3211c5.nq.gz
│   ├── b38506549ff4f5c702c003592e64a72febb5a4e3.nq.gz
│   ├── bc00b31e41c7af336ca01be967ec5d264553dc49.nq.gz
│   ├── bc81da7b97b7b3b96ef41c63583e83eb39c15bf8.nq.gz
│   ├── c7c98099a5759b6b4295263362fa6902be3c3284.nq.gz
│   ├── c853585163e6641d2480f1f8bda798b183e9f10e.nq.gz
│   ├── d5bea2e6510601cf86b813eb66e7be0fa41c98bc.nq.gz
│   ├── f3a81eda2e2d7a03236ff052148ec7724c915179.nq.gz
│   ├── f3de5772d1ef4addc4e2e2573040baf23517d029.nq.gz
│   ├── f7c9b387ff0b62ac249f00c3ca7e73e473aadc50.nq.gz
│   └── fc6c4b5e3d179c59fa9edeb80a3f5ceb6089e749.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7ed360b795ab66cdb78c365fd136a82c524c0127.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[TopQuadrant/shacl-js](https://github.com/TopQuadrant/shacl-js)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
