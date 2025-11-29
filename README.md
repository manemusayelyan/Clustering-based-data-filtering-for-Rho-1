# **Clustering-based data filtering for Rho-1**

Training TinyLlama-1B on the same set as Rho-1 but with a new type filtering inspired by [1]. Using hierarchical clustering on token representations that are computed using the reference model (keeping the contexts).

Inspired by:

**1.  [Automatic Data Curation for Self-Supervised Learning: A Clustering-Based Approach](https://arxiv.org/abs/2405.15613)**

**2.  [Rho-1:Not All Tokens Are What You Need](https://arxiv.org/abs/2404.07965)**
