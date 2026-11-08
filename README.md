# Repolex Knowledge Graph of modal-labs/modal-cursor

RDF knowledge graph data for [modal-labs/modal-cursor](https://github.com/modal-labs/modal-cursor), parsed by [repolex](https://repolex.ai).

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
rlex download modal-labs/modal-cursor
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 954c0123d69cd93721fed29850c46beba708cfd6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 954c0123d69cd93721fed29850c46beba708cfd6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0524f4b1fe8b98635c3d49ad87885032bb886fa9.nq.gz
│   ├── 0d4090f4de153cdee564460ff5d4389e1081a856.nq.gz
│   ├── 11552488c98e2b887b426e0c4b05b132afed3d5e.nq.gz
│   ├── 1cf453d7f9cd22d61332e292f62a2614e2d93577.nq.gz
│   ├── 22782810c461d8f26acaf0489d5cb442987bae4d.nq.gz
│   ├── 2ffdae7724f6633fdc843487a49cd3795a19cd5b.nq.gz
│   ├── 373e0fcd78a2624d9ba4d810755b404545ffb9ac.nq.gz
│   ├── 3cabbda1977adb0d6c808bad32e822b52ea72351.nq.gz
│   ├── 3ecc36cd73c2f2ab96fcde568056e37fd209d662.nq.gz
│   ├── 49bf144142982a3847bfe20c95f09b2bb4cd6a76.nq.gz
│   ├── 49e6a135863528004d63e690165bdc1934517dcb.nq.gz
│   ├── 5480f03197bb3995d6be45fe8f00eca5548216f0.nq.gz
│   ├── 6324d401a069f4020efcf0ff07442724b52f47c2.nq.gz
│   ├── 6462cf556ebfbeab79f7e13bf578f96c4f142160.nq.gz
│   ├── 6ecefb9a48af684c19e9b671785a091d477f0cf8.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 8ca8fb28969b0f768b77bdb25e648cbde82f477c.nq.gz
│   ├── b72c67109598b2f628683aa8203702cd491a6136.nq.gz
│   ├── bc3a61eb8791864dc6e736a78e71184a1ac3459c.nq.gz
│   ├── bf23728c14de662bb90956316a0cd09278374685.nq.gz
│   ├── ca05789dfd041d36a33ddf5c4444801d192e89ed.nq.gz
│   ├── d0038c5708922a25811b05039ba0d68156c061c1.nq.gz
│   ├── d7e9d546144623fd7f55d4b55518bddaabf20e54.nq.gz
│   ├── dbae44dfc985299ba2d5f3209c370c89bf04d831.nq.gz
│   ├── e1378c5234b610981330d434c0547f30d0456736.nq.gz
│   ├── e4eff9a9df470e93a0c42cead7ae8a409e3aa1e4.nq.gz
│   ├── e52854c43478c31552e65ef4fec047b8f6e217c9.nq.gz
│   ├── e915ffc543485ec3a1805e1d26c5711135b4580b.nq.gz
│   ├── f92007c6a282b10b4f40581f3139b972fbcfa51b.nq.gz
│   └── f9f2bb41a6527547242ddafd0a7b7b07b3dde190.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 954c0123d69cd93721fed29850c46beba708cfd6.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 37 files
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

[modal-labs/modal-cursor](https://github.com/modal-labs/modal-cursor)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
