---
title: "Uniformly Optimal and Parameter-free First-order Methods for Convex and Function-constrained Optimization"
collection: publications
category: preprint
date: 2024-12-09
paperurl: 'https://arxiv.org/pdf/2412.06319'
---

This paper presents new first-order methods for achieving optimal oracle complexities in convex optimization with convex functional constraints. Oracle complexities are measured by the number of function
and gradient evaluations. To achieve this, we enable first-order methods to utilize computational oracles
for solving diagonal quadratic programs in subproblems. For problems where the optimal value f* is
known, such as those in overparameterized models and feasibility problems, we propose an accelerated
first-order method that incorporates a modified Polyak step size and Nesterov's momentum. Notably, our
method does not require knowledge of smoothness levels, Hölder continuity parameter of the gradient, or
additional line search, yet achieves the optimal oracle complexity bound of O(ε⁻²/⁽¹⁺ᵖ⁾) under Hölder
smoothness conditions. When f* is unknown, we reformulate the problem as finding the root of the optimal value function and develop inexact fixed-point iteration and secant method to compute f*. These
root-finding subproblems are solved inexactly using first-order methods to a specified relative accuracy.
We employ the accelerated prox-level (APL) method, which is proven to be uniformly optimal for convex optimization with simple constraints. Our analysis demonstrates that APL-based level-set methods
also achieve the optimal oracle complexity of O(ε⁻²/⁽¹⁺ᵖ⁾) for convex function-constrained optimization, without requiring knowledge of any problem-specific structures. Through experiments on various
tasks, we demonstrate the advantages of our methods over existing approaches in function-constrained
optimization.