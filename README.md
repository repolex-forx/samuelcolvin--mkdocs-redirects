# Repolex Knowledge Graph of samuelcolvin/mkdocs-redirects

RDF knowledge graph data for [samuelcolvin/mkdocs-redirects](https://github.com/samuelcolvin/mkdocs-redirects), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/mkdocs-redirects
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 32ccfd0ce36bcd25df66a5c58a3e1a0916f2a767
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 32ccfd0ce36bcd25df66a5c58a3e1a0916f2a767
│           └── chunk-001.nq.gz
├── blob
│   ├── 103d9406081972f556de341bb01a01c5068ae60c.nq.gz
│   ├── 4367dddbac307fbeda789ac1e066c0f8f5020b26.nq.gz
│   ├── 44fed5b21225af728118d11a0ca12316db50b200.nq.gz
│   ├── 636f30a2f382d570a9c888555071a74e39417f30.nq.gz
│   ├── 6887eaabd141bd6f5c048826e2da9431835e8939.nq.gz
│   ├── 6fee1c3d77326f9dbc2885dd5aa2db77445a6592.nq.gz
│   ├── 79291e6c45f32a8544a0e1ae32b01ac45bf0ffa9.nq.gz
│   ├── 9264cb0a9480fa4b6cc9de9de1ca0f74d60ebd20.nq.gz
│   ├── 9a8b9ab8c7dd0224e3f315811b2a3495e428992b.nq.gz
│   ├── 9d58bd5025503f08a7038b146d479757271b89c5.nq.gz
│   ├── a955fdae12bdf32b79296a3a6dd424aac3843677.nq.gz
│   ├── d0d23352ea08c8e31b465da4e9f270458d6d52bf.nq.gz
│   ├── d53332ade14644f34b4b626a28036c816e6ab3e8.nq.gz
│   └── f86c713df4fc459da4c73ff4fa9e5cfde4dc67a9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 32ccfd0ce36bcd25df66a5c58a3e1a0916f2a767.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 21 files
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

[samuelcolvin/mkdocs-redirects](https://github.com/samuelcolvin/mkdocs-redirects)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
