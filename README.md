# MPI-Heterogeneity-RainbowTables-Experiment-Data

This repository contains experimental data supporting the study titled **"Parallel Algorithm for Rainbow Tables Generation on Heterogeneous CPU Cluster"** (forthcoming).

## Overview

The experiments evaluate a parallel algorithm for rainbow table generation on a **heterogeneous CPU cluster**, where compute nodes differ in processing capability. A newly proposed load-balancing scheme (**new**) is compared against the baseline scheme (**old**) across four cryptographic hash functions: NTLM, MD5, SHA-256, and SHA-512. The primary metrics assessed are execution time, speedup, efficiency, and load imbalance, measured as the number of cores is scaled from 1 to 80.

## Data Description

The data is organized into two directories. In every file, `core_count` is the number of CPU cores used (1–80), and results are reported for each of the four hash functions.

### `performance/`

Raw performance measurements for the rainbow table generation runs. Files are provided in **new/old** pairs so the proposed and baseline algorithms can be compared directly.

Columns: `core_count`, `execution_time`, `speedup`, `efficiency`

- **new_perf_rtgen_NTLM.csv** — Proposed algorithm, NTLM.
- **new_perf_rtgen_MD5.csv** — Proposed algorithm, MD5.
- **new_perf_rtgen_SHA256.csv** — Proposed algorithm, SHA-256.
- **new_perf_rtgen_SHA512.csv** — Proposed algorithm, SHA-512.
- **old_perf_rtgen_NTLM.csv** — Baseline algorithm, NTLM.
- **old_perf_rtgen_MD5.csv** — Baseline algorithm, MD5.
- **old_perf_rtgen_SHA256.csv** — Baseline algorithm, SHA-256.
- **old_perf_rtgen_SHA512.csv** — Baseline algorithm, SHA-512.

### `load-imbalance/`

Load-imbalance measurements across the cluster for each hash function, with the baseline and proposed schemes reported side by side in a single file.

Columns: `core_count`, `load_imbalance_old`, `load_imbalance_new`

- **load_imbalance_NTLM.csv** — Load imbalance (old vs. new), NTLM.
- **load_imbalance_MD5.csv** — Load imbalance (old vs. new), MD5.
- **load_imbalance_SHA256.csv** — Load imbalance (old vs. new), SHA-256.
- **load_imbalance_SHA512.csv** — Load imbalance (old vs. new), SHA-512.

## Citation

**Vainer, M.**, Kačeniauskas, A., & Goranin, N. Parallel Algorithm for Rainbow Tables Generation on Heterogeneous CPU Cluster. Electronics, 15(16), 3596. https://doi.org/10.3390/electronics15163596
