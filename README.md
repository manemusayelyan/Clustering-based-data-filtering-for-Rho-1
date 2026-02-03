# **Clustering-based data filtering for Rho-1**

Training TinyLlama-1B on the same set as Rho-1 but with a new type filtering inspired by [1]. Using hierarchical clustering on token representations that are computed using the reference model (keeping the contexts).

Inspired by:

**1.&nbsp; [Automatic Data Curation for Self-Supervised Learning: A Clustering-Based Approach](https://arxiv.org/abs/2405.15613)**

**2.&nbsp; [Rho-1:&nbsp;Not All Tokens Are What You Need](https://arxiv.org/abs/2404.07965)**

## Benchmark Comparison

The baseline model `TinyLlama/TinyLlama-1.1B-intermediate-step-1431k-3T` was evaluated on the exact set of benchmark tasks used by the Rho-1 authors. The comparison results are shown in the table below.

| Evaluation | GSM8K | SVAMP | ASDiv | MAWPS | TAB | MQA | MMLU STEM | SAT‡ | MATH |
|------------|-------|-------|-------|-------|-----|-----|-----------|------|------|
| TinyLlama/TinyLlama-1.1B-intermediate-step-1431k-3T (Rho-1 paper) | 2.9 | 11.0 | 18.1 | 20.4 | 12.5 | 14.6 | 16.1 | 21.9 | 3.2 |
| TinyLlama/TinyLlama-1.1B-intermediate-step-1431k-3T (My eval) | 2.9 | 10.7 | 17.8 | 20.2 | 12.3 | 14.2 | 16.2 | 21.9 | 2.1 |

