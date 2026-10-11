# Repolex Knowledge Graph of python-hyper/priority

RDF knowledge graph data for [python-hyper/priority](https://github.com/python-hyper/priority), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/priority
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 532ace514de40ebf9a9c0a4418cbfb0e72c8f7a4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 532ace514de40ebf9a9c0a4418cbfb0e72c8f7a4
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a3b8703d568a951119da2630fb387fb9fb83854.nq.gz
│   ├── 20691ead64c657e8a2b26ed3bb755fa5894ffe96.nq.gz
│   ├── 235c53fd20384e49160eff65e59188a5103849df.nq.gz
│   ├── 28619453f1ad512c99f8e51b4589a995766207c0.nq.gz
│   ├── 29997f2aa2fcc51a60813967b26df3c5288a05c7.nq.gz
│   ├── 5352d024fb0c6f7eeaab156a0406c12e84d1117f.nq.gz
│   ├── 5d745f9d2ec3a81aecfff53f0e9bcfc0b78201f1.nq.gz
│   ├── 5e036d9c4f25be8b130918d3cad733caeff2bd79.nq.gz
│   ├── 6cd34d1ebe1791d14c0c50929c7fe44addf3a908.nq.gz
│   ├── 73d5e888192e9d009790e5beb841e69e82086745.nq.gz
│   ├── 7c26cbed568cd6b2cc101e443908a73077eb2467.nq.gz
│   ├── 8af19477e20681aeff4086b5afa87e6eabcceca2.nq.gz
│   ├── a05e54ceffb20e3cf91d70d9ce04d16dce20653a.nq.gz
│   ├── a05fb3f5b41e2e8cb5b3d29723eb6739ba046d00.nq.gz
│   ├── a79157c52780373cb92d5674174df677c0b4eac0.nq.gz
│   ├── ab3e4b69df6a9c02f4adf23d5c8e1dd361cf775f.nq.gz
│   ├── c7e4d843afcb919cb99be8ccbb07e97647ef48be.nq.gz
│   ├── d6466b602473a2683ccf84a9f6c6dce140a058e3.nq.gz
│   ├── db2472009c60acc72ca2f6f065bb4b674dc66746.nq.gz
│   ├── e2a9b28036b2fdaa4d3104030ee46611085ab772.nq.gz
│   ├── e405381af5615e39c8317151a1c84154eb031cb3.nq.gz
│   ├── e4f77c41f2ea2919688f915dbbf74704ef426a44.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9fb93840e30fcc03295900c352d074824ca6fea.nq.gz
│   ├── ec94b7171512e082a4b356d35e0c86dad94aea19.nq.gz
│   └── f9cff2e8d92093ca65514da547f93e3ef183adcd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 532ace514de40ebf9a9c0a4418cbfb0e72c8f7a4.nq.gz
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

[python-hyper/priority](https://github.com/python-hyper/priority)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
