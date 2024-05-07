---
title: "A Review on Principal Stratification with Noncompliance and Missing Outcome Data via Mixture Model"
tags:
  - Causal Inference
  - Statistical Analysis
  - Estimation
---

This project was completed as an independent final study for the Spring 2024 section of [STA 640: Causal Inference](https://www2.stat.duke.edu/~fl35/CausalInferenceClass.html) at Duke University.

🚩 **Keywords: Principal Stratification, Rubin Causal Model, Noncompliance, Partially Defined Outcomes, Bayesian Pattern Mixture Model, Finite Mixture Model, Expectation-Maximization (EM) Algorithm, Missing at Random (MAR)**

After pursuing deeper into causal inference, the topic of noncompliance fascinates me. In a common setting, we expect a completely randomized study between the treatment and control arms, such that Z —> Y. However, sometimes confounding occurs post-treatment (i.e., different from the pre-treatment confounders relating to covariates), such that a post-treatment confounder D happens after Z but before Y: Z —> D —> Y. Such D can be an indicator of selection bias, censored / truncated variable by death, or noncompliance from subjects (i.e., not following the assigned treatment). Accompanying noncompliance is also the issue of partially defined outcomes, where the outcomes Y is partially obtainable due to noncompliance of some subject units. 

To address the complications in discussion, the *principal stratification* (PS) framework comes back to sight, paired with *potential outcomes* and Rubin causal model (RCM), to offer solution on the solid groundwork by instrumental variable (IV) studies. Under PS, we subgroup subjects into principal strata based on their potential outcomes of D(z). During estimation, since the PS memberships of each subject is unobservable, we usually include well-defined assumptions to aid our estimation based off of the mixture strata, or denote estimands of our own (from the most common PCE and CACE to more granular estimands). As per the nature of the mixture strata, adopting a latent mixture model structure may come to the rescue. Popular approach in mixture models include:

- Direct likelihood mixture 
- Likelihood-based mixture + Expectation-maximization (EM) algorithm
- Bayesian mixture

In this paper, I reviewed two classic studies by Barnard et al. (2003) and Frumento et al. (2012), both of whom attempt to approach noncompliance under PS, but adopt different modeling strategies (Bayesian and likelihood + EM, respectively). Each study has been organized into the following parts: [Background] - [Goal] - [Method] - [Variables Defined] - [Estimands] - [Assumptions] - [Modeling] - [Results]. Hopefully, you will gain a deeper interest into the topic and understand some of the pros and cons of different models with comparative thinking!


<embed src="https://hollyyfc.github.io/docus/STA640-Final.pdf" width="800" height="600" type="application/pdf">

  <br>
  
### Reference

Barnard, John, Constantine E Frangakis, Jennifer L Hill, and Donald B Rubin. 2003. “*Principal Stratification Approach to Broken Randomized Experiments.*” Journal of the American Statistical Association 98 (462): 299–323. https://doi.org/10.1198/016214503000071.

Frumento, Paolo, Fabrizia Mealli, Barbara Pacini, and Donald B. Rubin. 2012. “*Evaluating the Effect of Training on Wages in the Presence of Noncompliance, Nonemployment, and Missing Outcome Data.*” Journal of the American Statistical Association 107 (498): 450–66. http://www.jstor.org/stable/23239583.










