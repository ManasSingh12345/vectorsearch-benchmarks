# Sweep definitions

Pass any file here to `run_sweep.sh` with `--sweeps sweeps/<file>.json`.

| File | Description |
|------|-------------|
| `default.json` | Upstream default sweep |
| `test_1M.json` | Small 1M wiki smoke (CAGRA_SEARCH + CAGRA_HNSW) |
| `cagra_search_grid_1M.json` | Full CAGRA_SEARCH NN_DESCENT grid (wiki 1M) |
| `cagra_search_grid.json` | CAGRA_SEARCH grid (10M dataset name) |
| `cagra_search_sw128_retest_1M.json` | Single sw128 failure retest |
| `hnswlib_base_1M.json` | LUCENE_HNSW hnswlib-style grid |
| `lucene_hnsw_test_1M.json` | Single LUCENE_HNSW smoke |
| `cagra_ivfpq_1M.json` | CAGRA_SEARCH + CAGRA_HNSW, IVF_PQ build |
| `trials/0/`, `trials/1/` | Historical trial sweeps |

Example:

```bash
./run_sweep.sh --data-dir /raid/workspace/data \
  --datasets datasets_test_1M.json \
  --sweeps sweeps/cagra_ivfpq_1M.json \
  --configs-dir configs_cagra_ivfpq_1m \
  --results-dir results \
  --run-benchmarks
```
