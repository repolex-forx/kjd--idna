# Repolex Knowledge Graph of kjd/idna

RDF knowledge graph data for [kjd/idna](https://github.com/kjd/idna), parsed by [repolex](https://repolex.ai).

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
lexq download kjd/idna
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 729225d8b0c58bc66bb38d1d0faf281a757ece59
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 729225d8b0c58bc66bb38d1d0faf281a757ece59.nq.gz
│   └── repolex
│       └── 729225d8b0c58bc66bb38d1d0faf281a757ece59
│           └── chunk-001.nq.gz
├── blob
│   ├── 147a968ecbba5b58e7738dc565c3d02f074cc83b.nq.gz
│   ├── 19b6b45242c16a1025465309eec2ca5009319de3.nq.gz
│   ├── 1df9f2a70e6815908f2784e88897a9a359eef84c.nq.gz
│   ├── 28c5b64e0e9936ece5ba06b27e5ad86df939d34f.nq.gz
│   ├── 4be6004622efcdc36a8d15efc0ac3e138a4bae02.nq.gz
│   ├── 514ff7e2e68b65f309d30a0b06e6b290d2c353a8.nq.gz
│   ├── 5b8b9f336a79b0b9e8dd222512a7b9377aa214c1.nq.gz
│   ├── 5c44ec137cb04b9911b331ded5e5d96ab89c4aa1.nq.gz
│   ├── 5f5bd3820ee0770f9779309c31de1aec9de553d4.nq.gz
│   ├── 5f7147fc26c373b66c9c448d304d0a71eb467269.nq.gz
│   ├── 7bfaa8d80d7dc471d572db0f949460901126e8bd.nq.gz
│   ├── 835e6c67b07766e6e20ebf9f46a2075e678c8713.nq.gz
│   ├── 9009ae9893023dc7edbaf14d620e37f7986fb65c.nq.gz
│   ├── 9115f123f0274832af5ba1cf3c5481cc5353eecd.nq.gz
│   ├── 913abfd6a23ce547f84de2adc41221012f1007d6.nq.gz
│   ├── 951f75dbba6344da6f769bf835545745bfa93fb6.nq.gz
│   ├── 9e1eda72c6611e0af6249b8f7dbc589fec92ba8d.nq.gz
│   ├── aacdecfb7fb951c345190852aea5f4fd80cb8f1f.nq.gz
│   ├── b59f5e50de896650005bea3a4ea8091702f7c66b.nq.gz
│   ├── cc71c78bd1e639dc633c170593d5951c4e45a378.nq.gz
│   ├── cfdc030a751b089fc7e38fc88093b791605d501d.nq.gz
│   ├── d8456a1cc1b9345346587977e21075118c463e68.nq.gz
│   ├── dcff6940b52f6a2e64115ce3b5cba555c4add12c.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb894327410debecb64ddf40eddc3131cf8344de.nq.gz
│   └── f4a007f26068b26e5a9a960b442529ffba05a4fb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 729225d8b0c58bc66bb38d1d0faf281a757ece59.nq.gz
├── filetree
│   └── 729225d8b0c58bc66bb38d1d0faf281a757ece59.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 36 files
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

[kjd/idna](https://github.com/kjd/idna)

---
*Parsed on 2026-04-13 by [repolex](https://repolex.ai)*
