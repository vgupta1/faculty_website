---
title: Small-Data, Large-Scale Linear Optimization
shorttitle: SmallData
journal: Management Science (Minor Revision)
authors: Paat Rusmevichientong
sort_order: 9
pdf_path: SmallData_WP.pdf
links:
  - name: Code on GitHub
    path: https://github.com/vgupta1/EmpBayes
  - name: SSRN
    path: https://ssrn.com/abstract=3065655
---
Optimization applications often depend upon a huge number of uncertain parameters.  In many contexts, however, the amount of relevant data per parameter is small, and hence,  we may only have  imprecise estimates.  We term this setting -- where the number of uncertainties is large, but all estimates have low precision -- the "small-data, large-scale regime."  We formalize a model for this new regime, focusing on optimization problems with uncertain linear objectives.  We show that common data-driven methods may perform poorly in this new setting, despite their provably good performance in the traditional large-sample regime.  Such methods include sample average approximation, "estimate-then-optimize" policies, data-driven robust optimization, and certain regularized policies.  

We then propose a novel framework for selecting a data-driven policy from a given policy class.  Like the aforementioned data-driven methods, our policy enjoys provably good performance in the large-sample regime.  Unlike, these methods, however, we show 
that in the small-data, large-scale regime, our data-driven policy performs comparably to an oracle best-in-class policy, provided the policy class and estimates satisfy some mild conditions.  We specialize and strengthen this result for linear optimization problems and two natural policy classes: the first inspired by the empirical Bayes literature in statistics and the second by the regularization literature in optimization and machine learning.  For both classes, we show that the suboptimality gap between our proposed policy and the oracle policy decays exponentially fast in the number of uncertain parameters, even for a fixed amount of data.  Thus, these policies retain the strong large-sample performance of traditional methods, and additionally enjoy provably strong performance in the small-data, large-scale regime. Numerical experiments confirm the significant benefits of our methods.

