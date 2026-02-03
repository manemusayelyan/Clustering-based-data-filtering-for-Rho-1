# Clustering-based data filtering for Rho-1

Training TinyLlama-1B on the same set as Rho-1 but with a new type of filtering inspired by the works below. Using hierarchical clustering on token representations that are computed using the reference model (keeping the contexts).

### Inspired by:
1. [Automatic Data Curation for Self-Supervised Learning: A Clustering-Based Approach](https://arxiv.org/abs/2405.15613)
2. [Rho-1: Not All Tokens Are What You Need](https://arxiv.org/abs/2404.07965)

---

## Benchmark Comparison

The baseline model `TinyLlama/TinyLlama-1.1B-intermediate-step-1431k-3T` was evaluated on the exact set of benchmark tasks used by the Rho-1 authors. The comparison results are shown in the table below.

| Evaluation        | GSM8K | SVAMP | ASDiv | MAWPS | TAB | MQA | MMLU STEM | SAT‡ | MATH |
|-------------------|-------|-------|-------|-------|-----|-----|-----------|------|------|
| TinyLlama-1.1B-intermediate-step-1431k-3T (Rho-1 paper) | 2.9 | 11.0 | 18.1 | 20.4 | 12.5 | 14.6 | 16.1 | 21.9 | 3.2 |
| TinyLlama-1.1B-intermediate-step-1431k-3T (My eval) | 2.9 | 10.7 | 17.8 | 20.2 | 12.3 | 14.2 | 16.2 | 21.9 | 2.1 |

---

## Continual Pretraining (CPT) Results

Performed continual pretraining (CPT) of TinyLlama-1.1B on the OpenWebMath dataset following the RHO-1 study. The table below compares our CPT results with the results reported by the RHO-1 authors.

| Evaluation | GSM8K | SVAMP | ASDiv | MAWPS | TAB | MQA | MMLU STEM | SAT‡ | MATH |
|------------|-------|-------|-------|-------|-----|-----|-----------|------|------|
| TinyLlama-CT (Rho-1 paper) | 6.4 | 21.7 | 36.7 | 47.7 | 17.9 | 13.9 | 23.0 | 25.0 | 2.4 |
| TinyLlama-CT (My eval) | — | — | — | — | — | — | — | — | — |

> **Note:** The RHO-1 CPT model was not publicly released; comparisons are based on reported metrics.sed; comparisons are based on reported metrics.
