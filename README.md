# Repolex Knowledge Graph of ansible-community/lightspeed-analysis-framework

RDF knowledge graph data for [ansible-community/lightspeed-analysis-framework](https://github.com/ansible-community/lightspeed-analysis-framework), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/lightspeed-analysis-framework
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 27c76f2f89cd7b11c05aa54abffa422b9858a990
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 27c76f2f89cd7b11c05aa54abffa422b9858a990
│           └── chunk-001.nq.gz
├── blob
│   ├── 1522a74f3a34134decab5e5437785b2b6a26c5b7.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 41dbaa172ae30837b972b4e77ef2e26a68e3dc0b.nq.gz
│   ├── 56eec7d40dd9396ddceb1498aa28cdf95a0a7c95.nq.gz
│   ├── 753adfbe70e0e6078f9afeb38749cee79e366aa1.nq.gz
│   ├── 892aeafd5213011db36997efcd14ef5d61be6ecf.nq.gz
│   ├── 8998330b78cc23156820e85c7c5fce717fa19ec6.nq.gz
│   ├── 952a7f45d19a736869212e97830737c4815c21d9.nq.gz
│   ├── 9a8da14bab4b15f798b4ee757e1c96d0991f9dbc.nq.gz
│   ├── 9b2be5703d311fc095f02e8ada6d2e2b26b28643.nq.gz
│   ├── a02f13beaef238365d086df814a601e18fb9415a.nq.gz
│   ├── a223f75ceaf90c52d46232acf89bc5e29fb112d5.nq.gz
│   ├── ad1c79c729f3c281d1c9d1fb00e3939f46bf00f8.nq.gz
│   ├── b5562c5a79944d8d7c8bc349688e0a8faf60d378.nq.gz
│   ├── be4a62c8af1dd5959819c115cb7c8f820531b800.nq.gz
│   ├── c1a19a16dca0f9951883ba65e073d99e6ddd0e69.nq.gz
│   ├── c31d6d0ab3a3e6d12ff1a82676d9cd2ad6d78a09.nq.gz
│   ├── dabe38e1eabe119e5fff68e0b99d475b6c42bb63.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 27c76f2f89cd7b11c05aa54abffa422b9858a990.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 26 files
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

[ansible-community/lightspeed-analysis-framework](https://github.com/ansible-community/lightspeed-analysis-framework)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
