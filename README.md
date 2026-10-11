# Repolex Knowledge Graph of pytest-dev/nose2pytest

RDF knowledge graph data for [pytest-dev/nose2pytest](https://github.com/pytest-dev/nose2pytest), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/nose2pytest
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 15ca467f518e828262c068cb8cce3aa666ce8267
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 15ca467f518e828262c068cb8cce3aa666ce8267
│           └── chunk-001.nq.gz
├── blob
│   ├── 0892383b10eb72bfc5ab668c42113a0cd2a1311b.nq.gz
│   ├── 0c27bbdc1a18ec40da757ddd561f0ceb7ca94577.nq.gz
│   ├── 166725ab442dd8217b3f44a77ed63ea4480851fd.nq.gz
│   ├── 1b53600d1dc3587a053bec5e22643ac71473b726.nq.gz
│   ├── 21f21d2f1b33a632eaf3fc78811a32a47673d8a1.nq.gz
│   ├── 3be82b84ecde6c981351f7fa41f7fdf540048fd6.nq.gz
│   ├── 92ec36717f472899445044a9bdbcf7d4135f57f0.nq.gz
│   ├── 981c4812079c4488c534c2c3403f452a5edadd93.nq.gz
│   ├── 9827560c329b00b0d7d2b8c1e90e102560784c70.nq.gz
│   ├── a7e9016d4c2a176f54676ce2111001030e3f24a5.nq.gz
│   ├── ac94ed4072e5880be84b3d3eb0565b71927702a4.nq.gz
│   ├── add5e80b5dc3b5b926ef0e7facf9c9dcf7500e13.nq.gz
│   ├── be006de9a1ae3b9628e796c74277cd6d61e0a34a.nq.gz
│   ├── cc02b338c015519674213856b552de65b865b2d7.nq.gz
│   ├── dc2b477a8fe7a6b6a839a4dc2a75e5d365ce1f97.nq.gz
│   ├── e13bd590c858eab2ba3506af867008063b736c2e.nq.gz
│   ├── e3287250de296b20f6fec8cf8986c4e23dc50aa1.nq.gz
│   ├── eb2e7d6fae454d698f128b03fd76c6c148d744e2.nq.gz
│   └── f61ca1ad664692dc2f8e0e4cbbddeca828054347.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 15ca467f518e828262c068cb8cce3aa666ce8267.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[pytest-dev/nose2pytest](https://github.com/pytest-dev/nose2pytest)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
