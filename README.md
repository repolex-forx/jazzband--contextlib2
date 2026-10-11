# Repolex Knowledge Graph of jazzband/contextlib2

RDF knowledge graph data for [jazzband/contextlib2](https://github.com/jazzband/contextlib2), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/contextlib2
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9a547a3247f5630e627b49b6971ec7a1d7ff6c23
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9a547a3247f5630e627b49b6971ec7a1d7ff6c23
│           └── chunk-001.nq.gz
├── blob
│   ├── 025e303ce77d8c007bbebe5edae11aa42584664c.nq.gz
│   ├── 0269b69c33fe464478878546f4843844de6f0f0a.nq.gz
│   ├── 2043285af54a30cb033a1960cf7763c9c33b12c3.nq.gz
│   ├── 275a1b42ba3cf6a6b82dc0d0cca7ce6a04d4ef99.nq.gz
│   ├── 29ac7cde561a8895738c996b8ba5e3b96d22c9e0.nq.gz
│   ├── 2d4b97787834140fd98d1c4f49a63fd968ce28cb.nq.gz
│   ├── 2e6def0ecd0b12ddcde29970df2ec91891e057e5.nq.gz
│   ├── 31dbf0d704ae126a6a14f5c1fb63ce6142bc100a.nq.gz
│   ├── 32e1550e2718580c2506a5c00c1a4682821a5da9.nq.gz
│   ├── 42b55027fed929ef0996a03151b4f45e5aebf88e.nq.gz
│   ├── 51c4b3323730820c7a42ea79e9b618b43962668c.nq.gz
│   ├── 5b5c01709494078497ee0ebd6d7da8fa2c6d47b8.nq.gz
│   ├── 61c24555056f0c2115d54150618ab5cee1a222ce.nq.gz
│   ├── 67e55b90dd984e79ed5a64d4b6131ba76859e494.nq.gz
│   ├── 67e734b5972ed645ca5550842618dedbad09e0aa.nq.gz
│   ├── 69468c90269c997cd77dc4ef00a0bfd98218e042.nq.gz
│   ├── 6c5d5d44e78ada9ae8ccbf17ec4f3bc72779ced0.nq.gz
│   ├── 70a775ab3c5798a35c3006bb70d6baf2d21c8cae.nq.gz
│   ├── 76f0bb288708b65f01f282ad41da24865076bd9f.nq.gz
│   ├── 8278201facd49f105679db17f56112e941a9b17a.nq.gz
│   ├── 8bf76938e37f2b8de010830f6092fd99431fe6a1.nq.gz
│   ├── 8df3cd0587c0890319df18e922c6ed5d42aed1b1.nq.gz
│   ├── a2cbaa642624392293bb18f74361287d1f685fff.nq.gz
│   ├── a637cd9f698b3fc1f9adc6d8b8ced6c5515e0202.nq.gz
│   ├── a6dade9b56377d798c2b43592d660f7671f78943.nq.gz
│   ├── a73b30915f6c951de029750806f23d251086e210.nq.gz
│   ├── b58136828fd486ab5622756c7f9a2dcde1303777.nq.gz
│   ├── b8121125cb56c7365f4cd33fa614e6a9a6c48ac2.nq.gz
│   ├── b9e91c7f1d52d17a94f298fcfe9e5444a906de80.nq.gz
│   ├── c285a8899d221c79f161d13cd7dd1e333f477e94.nq.gz
│   ├── c3fec94d94b3ea54da080e6f28d40566ad371292.nq.gz
│   ├── d0209523f19419a6ab67761b57f7c6acd836b7af.nq.gz
│   ├── d4c600ceecd4cb5917374737fa3fbd85667fbff4.nq.gz
│   ├── e0d5efab56fb94577e7804603eb6f21f36977cb2.nq.gz
│   ├── e40caa18c3f0d938aef1b032ad5127cab34ef492.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6e4a6fa2f49fbabd202d9e24f856c624197c74e.nq.gz
│   ├── ecba7163530d246448767be28d05b148d336e874.nq.gz
│   ├── f6669e01ae5cc99d2bfb29df4dfa284183264b30.nq.gz
│   └── fdc7c265e70359d3267ec3deb6f1d3bf8fcab0ae.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9a547a3247f5630e627b49b6971ec7a1d7ff6c23.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[jazzband/contextlib2](https://github.com/jazzband/contextlib2)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
