# Repolex Knowledge Graph of django-commons/drf-excel

RDF knowledge graph data for [django-commons/drf-excel](https://github.com/django-commons/drf-excel), parsed by [repolex](https://repolex.ai).

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
rlex download django-commons/drf-excel
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2d450c5b2aea0616515324b8c16a5049c4991906
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2d450c5b2aea0616515324b8c16a5049c4991906
│           └── chunk-001.nq.gz
├── blob
│   ├── 080cd49451f39bf3cb201c0bf54c37fc2ae09a44.nq.gz
│   ├── 0ab43b5657aa39fae28109ef5427fb21183d6305.nq.gz
│   ├── 140281c8bbce2109f4c48d29b5086336645e8ddb.nq.gz
│   ├── 24fd641bd55fad2c43e0a584c2c8dbcea1ca8e4c.nq.gz
│   ├── 2c39dc6762f80689603fd4039be27a9f58a118a9.nq.gz
│   ├── 309001ab23742987480bb5c962bbe6dbc5c7e0c5.nq.gz
│   ├── 31899837e68203201c029a17442fff21866565fd.nq.gz
│   ├── 493a04f1049d240fc4e8b0bc78974f67439bc5fb.nq.gz
│   ├── 537f3a113c6f6d59a7351cc8d02bc7cf25f929fd.nq.gz
│   ├── 55ba27563b38185d882d228ab921eedc5b7f1b1e.nq.gz
│   ├── 57c3bbdd5a0229dfd20397f5a97d8fee08008cc8.nq.gz
│   ├── 5e0ea8776f3ffe921cc0d77213cd6828a4d28455.nq.gz
│   ├── 6283075c9dd8f17208800b126b72125dd155a0e4.nq.gz
│   ├── 709a044d87bc397cad453d37dd1324eb173b5170.nq.gz
│   ├── 92f56b5608c8c79e2d72ccf8e7ef6f190839483b.nq.gz
│   ├── 9ac788b30421757b0022c42ec5e891a8e17b8a7d.nq.gz
│   ├── 9c1f9a7e91950b4d4671a5c2b4cac10c3764ffe0.nq.gz
│   ├── 9e9a1a13081072292e5978845ca7a611c80e814c.nq.gz
│   ├── acec5ee7ec05d829d35db944d3b42aa4c1f9e20a.nq.gz
│   ├── b2ae8c58c9f7859d0ffd1fabe55cb4540eb032f7.nq.gz
│   ├── b33d4aba5eec220dc252d5278eb2fb6dcf163b0a.nq.gz
│   ├── b39e014ee225831887463eae75b71ad03548c9a1.nq.gz
│   ├── bc582b0bed468c891a48ff1ed59cafb412acf0cc.nq.gz
│   ├── d5e80188a7ae2af7dd1a45e9a99bc2ef63a21714.nq.gz
│   ├── da284c8c5412b24ad4aba83fb5dd0f959eba4676.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f1ba909a08286c638124ced2ec6affbbd5946288.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2d450c5b2aea0616515324b8c16a5049c4991906.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[django-commons/drf-excel](https://github.com/django-commons/drf-excel)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
