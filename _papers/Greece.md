---
title: Efficient and Targeted COVID-19 Border Testing via Reinforcement Learning
shorttitle: Greece
journal: Nature
pub_date: Published online 22 Sept 2021
authors: Hamsa Bastani, Kimon Drakopoulos
sort_order: 12
pdf_path: GreeceCovid.pdf
awards: 
  - name: Finalist, 2021 Pierskalla Best Paper Competition (Winner to be announced at INFORMS!)
  - name: Finalist in the Post-Pandemic Supply-Chain and Healthcare Management Conference's Best Paper Competition
  - name: Spotlight Presentation at the Reinforcement Learning for Real-Life Workshop (ICML 2021)
links:
  - name: 10.1038/s41586-021-04014-z
    path: https://www.nature.com/articles/s41586-021-04014-z
  - name: SSRN
    path: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3789038
  - name: Open Source Algorithm
    path: https://github.com/vgupta1/EvaTargetedCovid19Testing
  - name: Code Supporting Paper
    path: https://github.com/vgupta1/EVA_CounterfactualAnalysis
---
(Formerly titled:  Deploying a Data-Driven COVID-19 Screening Policy at the Greek Border)

On July 1st, 2020, members of the European Union gradually lifted earlier COVID-19 restrictions
on non-essential travel. In response, we designed and deployed “Eva” – a novel reinforcement
learning system – across all Greek borders to identify asymptomatic travelers infected with
SARS-CoV-2. Eva allocates Greece’s limited testing resources based on demographic
characteristics and results from previously tested travelers to (i) limit the influx of new cases and
(ii) provide real-time estimates of COVID-19 prevalence to inform border policies.
Counterfactual analysis shows that Eva identified 1.85x as many asymptomatic, infected
travelers as random surveillance testing, with up to 2-4x as many during peak travel. Moreover,
Eva identified approximately 1.25-1.45x as many infected travelers as policies that require
similar infrastructure as Eva, but make allocations based on population-level epidemiological
metrics (cases/deaths/positivity rates) rather than reinforcement learning. Eva was also able to
identify countries with atypically high prevalence earlier than machine learning methods based
on epidemiological metrics alone, which allowed Greece to adaptively adjust border policies to
prevent additional infected travelers from arriving.
Finally, using Eva’s unique cross-country dataset on prevalence in asymptomatic, traveler
populations, we show that epidemiological metrics had limited predictive value for the actual
prevalence among asymptomatic travelers, and furthermore exhibited strong country-specific
idiosyncrasies in summer 2020. Our insights raise serious concerns about internationally
proposed border control policies [1] that are country-agnostic and based on population-level
epidemiological metrics. Instead, our work paves the way for leveraging reinforcement learning
and real-time data for public health goals, such as border control during a pandemic.  

Open-source code with a brief overview of the algorithm is also available above.  

Please see also:
 - [Nature News and Views](https://www.nature.com/articles/d41586-021-02556-w)
 - [Nature Editorial: Greece Used AI to Curb COVID](https://www.nature.com/articles/d41586-021-02554-y)
 - [USC News](https://news.usc.edu/192093/greece-covid-testing-travel-eva-algorithm-usc-study/)
 - [Webinar with Authors](https://www.marshall.usc.edu/news/project-eva-ai-covid-and-greek-tourism)
 - Other Popular News Coverage:  
   - [Entrepreneur](https://www.entrepreneur.com/article/363706)
   - [EurekAlert!](https://www.eurekalert.org/news-releases/929315)
   - [PhocusWire](https://www.phocuswire.com/algorithms-helped-bring-tourists-back-to-Greece)- [Travel Weekly Asia](https://www.travelweekly-asia.com/Destination-Travel/Reopening-to-tourism-It-s-all-Greek-to-me)
   - [USC Marshall News](https://www.marshall.usc.edu/news/data-driven-reopening)
   - [USC Press Release](https://pressroom.usc.edu/reopen-greek-economy/)



