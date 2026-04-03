# Repolex Knowledge Graph of asimov-platform/build-rust-action

RDF knowledge graph data for [asimov-platform/build-rust-action](https://github.com/asimov-platform/build-rust-action), parsed by [repolex](https://repolex.ai).

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
lexq download asimov-platform/build-rust-action
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 15c87d7d0f04601ad3de60cc971233da7ea3c402.nq.gz
│   │   ├── 3a4f96d9b47405e1f5b11fb75fbbfd70d97d4fde.nq.gz
│   │   └── aaff988b13b6a96b51ec44a4fc182697097a6bf7.nq.gz
│   ├── lsp
│   │   ├── 15c87d7d0f04601ad3de60cc971233da7ea3c402.nq.gz
│   │   ├── 3a4f96d9b47405e1f5b11fb75fbbfd70d97d4fde.nq.gz
│   │   └── aaff988b13b6a96b51ec44a4fc182697097a6bf7.nq.gz
│   └── repolex
│       ├── 15c87d7d0f04601ad3de60cc971233da7ea3c402.nq.gz
│       ├── 3a4f96d9b47405e1f5b11fb75fbbfd70d97d4fde.nq.gz
│       └── aaff988b13b6a96b51ec44a4fc182697097a6bf7.nq.gz
├── blob
│   ├── 23955edf6e81e1fbafe62246dbf15b7f0bddc4fd.nq.gz
│   ├── 5b6a90cb584e99dbe3f1345750b5c51e33dc14b0.nq.gz
│   ├── 6f7a55ff845441dff0091f64ac7ca49cd94e713a.nq.gz
│   ├── 6f7fbfa9683df2a9c6828053ba22f57dc9538550.nq.gz
│   ├── 9c6d4853922f5be63941f95f9c89834e56747601.nq.gz
│   ├── abe2f89221705a5bb3a4d365000a88266ef7f728.nq.gz
│   ├── dd1ba8ecbcab6530189b110e6eab58fba866271d.nq.gz
│   └── fdddb29aa445bf3d6a5d843d6dd77e10a9f99657.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   ├── 15c87d7d0f04601ad3de60cc971233da7ea3c402.nq.gz
│   ├── 3a4f96d9b47405e1f5b11fb75fbbfd70d97d4fde.nq.gz
│   ├── aaff988b13b6a96b51ec44a4fc182697097a6bf7.nq.gz
│   └── f0470f4a18e5824544cda9bfe5a9bc46a6a119b8.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 25 files
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

[asimov-platform/build-rust-action](https://github.com/asimov-platform/build-rust-action)

---
*Parsed on 2026-04-03 by [repolex](https://repolex.ai)*
