---
title: Interpretable Operations Research for High-Stakes Decisions&#58; Designing the Greek COVID-19 Testing System
shorttitle: GreeceWagner
journal: INFORMS Journal on Applied Analytics 
pub_date: 
authors: Hamsa Bastani, Kimon Drakopoulos
sort_order: 14
pdf_path: Wagner_Submission.pdf
links:
  - name: SSRN
    path: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3916367
awards: 
  - name: Winner of the 2021 Daniel H. Wagner Prize for Excellence in the Practice of Advanced Analytics and Operations Research 
---
In the summer of 2020, in collaboration with the Greek government, we designed and deployed Eva -- the first national scale, reinforcement learning system for targeted COVID-19 testing. In this paper, we detail the rationale for three major design/algorithmic elements: Eva's testing supply chain, estimating COVID-19 prevalence, and test allocation.
Specifically, we describe the design of Eva's supply chain to collect and process thousands of biological samples per day with special emphasis on capacity procurement. Then, we propose a novel, empirical Bayes estimation strategy to estimate COVID-19 prevalence among different passenger types with limited data and showcase how these estimates were instrumental for a variety of downstream decision-making. Finally, we propose a novel, multi-armed bandit algorithm that dynamically allocates tests to arriving passengers in a non-stationary environment with delayed feedback and batched decisions. All of our design and algorithmic choices emphasize the need for transparent reasoning to enable human-in-the-loop analytics. Such transparency was crucial to building trust and buy-in among policymakers and public health experts in a period of global crisis.

Please see also our partner paper --  Efficient and Targeted COVID-19 Border Testing via Reinforcement Learning -- above for more context on the Eva Project.