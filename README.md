# Repolex Knowledge Graph of agronholm/tzlocal

RDF knowledge graph data for [agronholm/tzlocal](https://github.com/agronholm/tzlocal), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/tzlocal
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5c5e35ec8c2b7fdd38702f9815368bb22b943a85
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5c5e35ec8c2b7fdd38702f9815368bb22b943a85
│           └── chunk-001.nq.gz
├── blob
│   ├── 000e051d88f6997f7c8f3762019d4d11ecde431e.nq.gz
│   ├── 028ec1d7acabc6b45220f83e2edef298070541a1.nq.gz
│   ├── 15be313c8119be0f81bee3e6d80325a405634049.nq.gz
│   ├── 258b393637294912a6d6c78973c09424136ed50e.nq.gz
│   ├── 2f01cab109846006945ee1ce8a517253144bd4bc.nq.gz
│   ├── 388273c2792cab7807377ec72f8d34f7218139d2.nq.gz
│   ├── 3d691c85aa28e5b5886f43308e7756c7bbaccdb4.nq.gz
│   ├── 4bdf8e68df04e19a0ec2242ad029c2d225c2c204.nq.gz
│   ├── 55f2b1920d63a9ef3db56fb0761379551ef6e496.nq.gz
│   ├── 6594dfdf3d9f0c77f72f8025a66a9a3feee39b05.nq.gz
│   ├── 698381f7ca79be44ee41c5b0ade986893e0bf15b.nq.gz
│   ├── 7e58cff33cd0a82448ee22a401e571a232f6fd48.nq.gz
│   ├── 7f193b3f2d9c0d1f26eb03152eed7ca352ef2c8e.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 95032934d63e86ca9e240657e9a0a403aa152b16.nq.gz
│   ├── 9be1d2fe595ad46b738cb22c44ed5eb559c29e82.nq.gz
│   ├── aa3231569c924288f09f9d775882779b7da90c62.nq.gz
│   ├── bd9d663e88e7c2212b73d7244812917256be870d.nq.gz
│   ├── c8196d66d9e2c754879e2639482000f1ffc28ab2.nq.gz
│   ├── e0feedbc8c1238f4915d9539588ab24525a7d366.nq.gz
│   ├── e1ddbfd6ec7f39e307b25fcd6f2e4e07dc5e4a27.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7003c44526a3109ee54b32c83ac945d29eb4555.nq.gz
│   ├── eaa0bdd8132d1485a5a9880a4988a6680fa0985c.nq.gz
│   └── fcc42a23f3f2183d5dd4ec58a731611a7fd4a03a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5c5e35ec8c2b7fdd38702f9815368bb22b943a85.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 31 files
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

[agronholm/tzlocal](https://github.com/agronholm/tzlocal)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
