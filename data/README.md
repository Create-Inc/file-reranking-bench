# FileRerankingBench Data

This directory contains the public benchmark fixtures and project corpora.

- `file-reranking-evals.json` contains prompts, candidate file metadata, and
  expected relevant file labels.
- `projects/<project>.zip` contains the corresponding project source tree rooted
  at `createxyz-project/`.

Fixture paths are app-root paths with a leading slash, such as
`/apps/web/pages/index/+Page.jsx`; remove the leading slash when resolving a
file inside the zip.
