---
title: Data-Driven Estimation in Equilibrium Using Inverse Optimization
authors: Dimitris Bertsimas and Ioannis Ch. Paschalidis
shorttitle: InvVI
journal: Mathematical Programming September 2014, Issue 0025-5610
sort_order: 3
pdf_path: InverseVIs.pdf
links:
  - name: doi:10.1007/s10107-014-0819-4
    path: http://link.springer.com/article/10.1007/s10107-014-0819-4
  - name: Code on Github
    path: https://github.com/vgupta1/InverseVIs
  - name: arXiv:1308.3397
    path: https://arxiv.org/abs/1308.3397
---
Equilibrium modeling is common in a variety of fields such as game theory and transportation science. The inputs for these models, however, are often difficult to estimate, while their outputs, i.e., the equilibria they are meant to describe, are often directly observable. By combining ideas from inverse optimization with the theory of variational inequalities, we develop an efficient, data-driven technique for estimating the parameters of these models from observed equilibria. We use this technique to estimate the utility functions of players in a game from their observed actions and to estimate the congestion function on a road network from traffic count data. A distinguishing feature of our approach is that it supports both parametric and \emph{nonparametric} estimation by leveraging ideas from statistical learning (kernel methods and regularization operators). In computational experiments involving Nash and Wardrop equilibria in a nonparametric setting, we find that a) we effectively estimate the unknown demand or congestion function, respectively, and b) our proposed regularization technique substantially improves the out-of-sample performance of our estimators.