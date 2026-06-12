# FileRerankingBench Results

These are aggregate numbers over the current public fixture set:

- 5 query fixtures
- 1 project corpus (`hiking-app-small`)
- 3 candidate files per query

Metrics are macro-averaged across query fixtures. For cases with no expected
relevant files, Recall@k is defined as 1.0. Precision@k is computed over the
files returned in the top-k window; because the current corpus has only three
candidates per query, Precision@5 and Precision@10 use the three available
candidates for the rank-all baselines below.

| System | Recall@1 | Precision@1 | Recall@3 | Precision@3 | Recall@5 | Precision@5 | Recall@10 | Precision@10 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Original candidate order | 0.6000 | 0.4000 | 1.0000 | 0.2667 | 1.0000 | 0.2667 | 1.0000 | 0.2667 |
| Recency baseline | 0.4000 | 0.2000 | 1.0000 | 0.2667 | 1.0000 | 0.2667 | 1.0000 | 0.2667 |
| Lexical baseline | 0.6000 | 0.4000 | 1.0000 | 0.2667 | 1.0000 | 0.2667 | 1.0000 | 0.2667 |
| Rank-all oracle upper bound | 1.0000 | 0.8000 | 1.0000 | 0.2667 | 1.0000 | 0.2667 | 1.0000 | 0.2667 |

The CSV version is available at `results/aggregate-results.csv`.

These results are published as benchmark reference numbers only. This repository
is limited to data, aggregate results, and the paper.
