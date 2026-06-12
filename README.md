# FileRerankingBench

Benchmark data and aggregate evaluation results for file selection in
code-editing LLM agents.

**Paper:** [FileRerankingBench: A Benchmark for File Selection in
Code-Editing Agents](paper.pdf) ([source](paper.tex))

**Authors:** Ahmad Jiha, Daniel Chen - Anything, Inc.

## Scope

This repository publishes the public benchmark artifact only:

- benchmark fixture data
- project corpora used by those fixtures
- aggregate evaluation numbers
- the paper source and PDF

This repository is deliberately limited to the public benchmark artifact and
does not include ranking-system source code or runtime details.

## Repository Layout

```text
data/
  file-reranking-evals.json     # Annotated benchmark fixtures
  projects/
    hiking-app-small.zip        # Project corpus used by the fixtures
results/
  aggregate-results.csv         # Aggregate metric table
RESULTS.md                      # Human-readable result summary
paper.tex
paper.pdf
```

## Benchmark Data

`data/file-reranking-evals.json` is an array of benchmark cases. Each case has:

| Field | Description |
| --- | --- |
| `input.project` | Project corpus name. |
| `input.userPrompt` | User request that requires selecting relevant files. |
| `input.files[]` | Candidate file paths and timestamp metadata. |
| `input.expectedRelevantFiles[]` | File paths labeled relevant for the prompt. |

The current public corpus contains five query fixtures over one small hiking app
project. Candidate paths are app-root paths such as
`/apps/web/pages/index/+Page.jsx`. The project zip stores files below
`createxyz-project/`; remove the leading slash from fixture paths when resolving
files inside the zip.

## Results

See [RESULTS.md](RESULTS.md) and
[results/aggregate-results.csv](results/aggregate-results.csv).

The published results are aggregate numbers over the public fixture set. They
are intended to anchor the benchmark and make future comparisons explicit
without expanding the repository beyond data, results, and the paper.

## Citation

```bibtex
@misc{jiha2026filererankingbench,
  title        = {FileRerankingBench: A Benchmark for File Selection in Code-Editing Agents},
  author       = {Ahmad Jiha and Daniel Chen},
  year         = {2026},
  howpublished = {\url{https://github.com/Create-Inc/file-reranking-bench}},
  note         = {Anything, Inc.}
}
```

## License

MIT.
