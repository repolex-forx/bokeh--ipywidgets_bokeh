# Repolex Knowledge Graph of bokeh/ipywidgets_bokeh

RDF knowledge graph data for [bokeh/ipywidgets_bokeh](https://github.com/bokeh/ipywidgets_bokeh), parsed by [repolex](https://repolex.ai).

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
rlex download bokeh/ipywidgets_bokeh
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 350a70e068324ecf6cfa762cc86bcb064fe724d6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 350a70e068324ecf6cfa762cc86bcb064fe724d6
│           └── chunk-001.nq.gz
├── blob
│   ├── 03bf2255eac56db0c8184cb99df186507bd5631b.nq.gz
│   ├── 05683e3e03f8357522848a8d78cef9ee039f20ff.nq.gz
│   ├── 06bc002bbc55f9fa027cdf6036163777eb080f07.nq.gz
│   ├── 0967ef424bce6791893e9a57bb952f80fd536e93.nq.gz
│   ├── 15058c70f862343f82999f47e840680d9746cb7b.nq.gz
│   ├── 1568182167d741f2ab949b571028593fddc2dd02.nq.gz
│   ├── 1a07a54c63d1de5cd43e28713fa3eee2da91c91d.nq.gz
│   ├── 294308a226ae8356ececc168f9e72039044055ee.nq.gz
│   ├── 2ea39577098d7c7af76b7b55f080f03ffa4eb383.nq.gz
│   ├── 3fa4ce9c306117e6538a5db0f2b9fc6f535da382.nq.gz
│   ├── 4321c286ef0e976602b58badd6e2a5fb40ab32da.nq.gz
│   ├── 467f56cb60de2672617651f5a6116e0a2e7d2ba2.nq.gz
│   ├── 4838f4fa9a2b30e7a8d3a1bf7998e0870154a09a.nq.gz
│   ├── 508bf291fe23c2e78596b3da7130be07e2452d28.nq.gz
│   ├── 532eec08f03b5f348020e60cfc66cc492bb5c55f.nq.gz
│   ├── 6337bfc3bf4140ae77677822b66677af921e990f.nq.gz
│   ├── 71cd046058764d2f74cc701a5b351418b58443a0.nq.gz
│   ├── 72b55a096ab1b48b088bd77efc89fc53a52ffaec.nq.gz
│   ├── 758436e88be219e64db66ad33374aee9f2efc87e.nq.gz
│   ├── 81d11a04183e3bdbae22b0aa1725fba6889b76cd.nq.gz
│   ├── 8ee6c1be621506bcad3e81572cf66a424e9f8b8a.nq.gz
│   ├── a2fea7a744ba36e825ccdaece81a885b2e9a1e1f.nq.gz
│   ├── a500c7d46887080e7725f58fe1803639112651ff.nq.gz
│   ├── a83b0dffb6ac436ab910ea02b28a2eb09db3cb85.nq.gz
│   ├── a8ed06904e4579b665189ca24bda17d182f0d1a0.nq.gz
│   ├── b5fff04b7656179debd4ad334027e32ae179dcc4.nq.gz
│   ├── b8d9000c6f152d084f483c6c57dd217d2da6cf08.nq.gz
│   ├── bd77f7fca9e237c2df58d4c9dc806142f1a40488.nq.gz
│   ├── cd84e65706a2c3e7773d83e65fcfd7940907a053.nq.gz
│   ├── d96c6f9e927e574e0360df16b2331ecee52f35f2.nq.gz
│   ├── df9c3b1dcdc47176a4acc14049efc451db768591.nq.gz
│   ├── e15356eab32d94ef4a6ca8d32ef7fbc725e06fb2.nq.gz
│   └── e32754c0d2a7a2f10f068a7de933fef12b7368b4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 350a70e068324ecf6cfa762cc86bcb064fe724d6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[bokeh/ipywidgets_bokeh](https://github.com/bokeh/ipywidgets_bokeh)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
