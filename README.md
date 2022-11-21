# PermLURM

##  Permutation-Based Hypothesis Testing in Local-to-Unity Regression Models 

### Description

The R package [‘PermLURM’](https://github.com/christiskatsouris/PermLURM) aims to implement a permutation-based approach for hypothesis testing for possibly  nonstationary autoregressive models and in general for local-to-unity regression models, including predictive regression models. In particular, this is a novel approach to existing methodologies such as the block-bootstrap based approach for unit root testing. However, the purpose of this research is to provide some evidence whether the proposed approach is a suitable alternative resampling method that ensures robust inference in these settings. 


<p align="center">
  
<img src="https://github.com/christiskatsouris/PermLURM/blob/main/data/persistence.jpg" width="460"/>

</p>  

We consider the following persistence classes:
   
#### (P1). nearly stable processes: 

$$\text{if} \ \ \left( \theta_n \right)_{ n \in \mathbb{N} } \ \ \text{is such that} \ \zeta = - \infty \ \ \text{and it holds that} \ \ \theta_n \to | \theta | < 1.$$
    
#### (P2). nearly unstable processes:   

$$\text{if} \ \ \left( \theta_n \right)_{ n \in \mathbb{N} } \ \ \text{is such that} \ \ \zeta \equiv c \in \mathbb{R} \ \ \text{and it holds that} \ \ \theta_n \to \theta = 1.$$

    
#### (P3). nearly explosive processes:   

$$\text{if} \ \ \left( \theta_n \right)_{ n \in \mathbb{N} } \ \ \text{is such that} \ \ \zeta = + \infty \ \ \text{and it holds that} \ \ \theta_n \to | \theta | > 1.$$

### Methodology  

The main challenging aspect with the proposed resampling method especially under the presence of the nuisance parameter of persistence is to accommodate the particular special dependence structure for the statistical problem of interest. 

## Installation (under development) 

The R package [‘PermLURM’](https://github.com/christiskatsouris/PermLURM) will be able to be installed from Github and CRAN.

## Usage 

```R

# After development the package will be able to be installed using
install.packages("PermLURM")
library("PermLURM")

```

## Notes:

1. This R package employs the novel IVX-P estimator proposed in the literature recently and aims to investigate the performance of the specific resampling method such as the permutation-based approach for robust statistical inference purposes in comparison to conventional method as well as the bootstrap-based approach. 

2.

# Key References:

$\textbf{[1]}$ Katsouris, C. (2022e). "A permutation-based approach for Hypothesis Testing in Nonstationary Autoregressive Regressions". University of Exeter. Working paper. 

$\textbf{[2]}$ Katsouris, C. (2021e). "Bootstrapping Nonstationary Autoregressive Processes in Predictive Regression". University of Southampton. Working paper.

$\textbf{[3]}$ Katsouris, C. (2020). "Treatment effect validation via a permutation test in Stata". University of Southampton. Working paper.

$\textbf{[4]}$ Demetrescu, M., Georgiev, I., Rodrigues, P. M., & Taylor, A. R. (2022). "Extensions to IVX methods of inference for return predictability". Journal of Econometrics. 

$\textbf{[5]}$ Chan, K. W. (2022). "Optimal difference-based variance estimators in time series: A general framework". The Annals of Statistics, 50(3), 1376-1400.

$\textbf{[6]}$ Austern, M., & Orbanz, P. (2022). "Limit theorems for distributions invariant under groups of transformations". The Annals of Statistics, 50(4), 1960-1991.

$\textbf{[7]}$ Kojevnikov, D. (2021). "The bootstrap for network dependent processes". arXiv preprint arXiv:2101.12312.

$\textbf{[8]}$ Cavaliere, G., & Georgiev, I. (2020). "Inference under random limit bootstrap measures". Econometrica, 88(6), 2547-2574.

$\textbf{[9]}$ Kostakis, A., Magdalinos, T., & Stamatogiannis, M. P. (2015). "Robust econometric inference for stock return predictability". The Review of Financial Studies, 28(5), 1506-1553.

$\textbf{[10]}$ Shao, X. (2010). "The dependent wild bootstrap". Journal of the American Statistical Association, 105(489), 218-235.

$\textbf{[11]}$ Jansson, M., & Moreira, M. J. (2006). Optimal inference in regression models with nearly integrated regressors. Econometrica, 74(3), 681-714.

$\textbf{[12]}$ Andrews, D. W. (2004). "The block–block bootstrap: improved asymptotic refinements". Econometrica, 72(3), 673-700.

$\textbf{[13]}$ Paparoditis, E., & Politis, D. N. (2003). "Residual‐based block bootstrap for unit root testing". Econometrica, 71(3), 813-855.

$\textbf{[14]}$ Carlstein, E., Do, K. A., Hall, P., Hesterberg, T., & Künsch, H. R. (1998). "Matched-block bootstrap for dependent data". Bernoulli, 305-328.

$\textbf{[15]}$ Lahiri, S. N. (1999). "Theoretical comparisons of block bootstrap methods". Annals of Statistics, 386-404.

$\textbf{[16]}$ Politis, D. N., & Romano, J. P. (1994). "The stationary bootstrap". Journal of the American Statistical association, 89(428), 1303-1313.
