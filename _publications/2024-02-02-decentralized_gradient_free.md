---
title: "Decentralized Gradient-Free Methods for Stochastic Non-smooth Non-convex Optimization"
collection: publications
category: conferences
date: 2024-02-02
paperurl: 'https://ojs.aaai.org/index.php/AAAI/article/view/29697'
---

We consider decentralized gradient-free optimization of minimizing Lipschitz continuous functions that satisfy neither smoothness nor convexity assumption. We propose two novel gradient-free algorithms, the Decentralized Gradient-Free Method (DGFM) and its variant, the Decentralized Gradient-Free Method+ (DGFM+). Based on the techniques of randomized smoothing and gradient tracking, DGFM requires the computation of the zeroth-order oracle of a single sample in each iteration, making it less demanding in terms of computational resources for individual computing nodes. Theoretically, DGFM achieves a complexity of O(d³/²δ⁻¹ε⁻⁴) for obtaining a (δ,ε)-Goldstein stationary point. DGFM+, an advanced version of DGFM, incorporates variance reduction to further improve the convergence behavior. It samples a mini-batch at each iteration and periodically draws a larger batch of data, which improves the complexity to O(d³/²δ⁻¹ε⁻³). Moreover, experimental results underscore the empirical advantages of our proposed algorithms when applied to real-world datasets.