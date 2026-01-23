---
title: "Optimal Methods for Unknown Piecewise Smooth Problems I: Convex Optimization"
collection: publications
category: preprint
date: 2026-01-022
paperurl: 'https://arxiv.org/abs/2601.14680'
---

We introduce an optimal and nearly parameter-free algorithm for minimizing piecewise smooth
(PWS) convex functions under the quadratic growth (QG) condition, where the locations and structure of the smooth regions are entirely unknown. Our algorithm, APEX (Accelerated Prox-Level
method for Exploring Piecewise Smoothness), is an accelerated bundle-level method designed to adaptively exploit the underlying PWS structure. APEX enjoys optimal theoretical guarantees, achieving
a tight oracle complexity bound that matches the lower bound established in this work for convex
PWS optimization. Furthermore, APEX generates a verifiable and accurate termination certificate,
enabling a robust, almost parameter-free implementation. To the best of our knowledge, APEX is
the first algorithm to simultaneously achieve the optimal convergence rate for PWS optimization and
provide certificate guarantees.