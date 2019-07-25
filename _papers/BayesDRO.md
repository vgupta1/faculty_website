---
title: Near-Optimal Bayesian Ambiguity Sets for Distributionally Robust Optimization
shorttitle: BayesDRO
journal: Management Science, March 2019.
sort_order: 7
pdf_path: Bayes_DRO_v5_final.pdf
links:
  - name: 10.1287/mnsc.2018.3140
    path: https://pubsonline.informs.org/doi/10.1287/mnsc.2018.3140
  - name: Code on GitHub
    path: https://github.com/vgupta1/AmbiguitySets
  - name: Optimization Online
    path: http://www.optimization-online.org/DB_HTML/2015/07/4983.html
---
We propose a Bayesian framework for assessing the relative strengths of data-driven ambiguity sets in distributionally robust optimization (DRO) when the underlying distribution is defined by a finite-dimensional parameter.  The key idea is to measure the relative size between a candidate ambiguity set and a specific, asymptotically optimal set.  This asymptotically optimal set is provably the smallest convex ambiguity set that satisfies a particular Bayesian robustness guarantee with respect to a given class of constraints as the amount of data grows large.  In other words, it is a subset of any other convex set that satisfies the same guarantee.  Using this framework, we prove that 
existing, popular ambiguity sets based on statistical confidence regions are significantly larger than the asymptotically optimal set with respect to constraints that are concave in the ambiguity-- the ratio of their sizes scales with the square root of the dimension of the ambiguity.  By contrast, we construct new ambiguity sets that are tractable, satisfy our Bayesian robustness guarantee with finite data and are only a small, constant factor larger than the asymptotically optimal set; we call these sets "Bayesian near-optimal."  We further prove that, asymptotically, solutions to DRO models with our Bayesian near-optimal sets enjoy frequentist robustness properties, despite their smaller size.  Finally, our framework yields guidelines for practitioners for selecting between competing ambiguity set proposals in DRO.  Computational evidence in portfolio allocation using real and simulated data confirms that our framework, although motivated by asymptotic analysis in a Bayesian setting, provides practical insight into the performance of various DRO models with finite data under frequentist assumptions.