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

## Univariate Permutation-Based Unit Root Testing

### Remarks:

Notice that permutation testing is a resampling methodology based on sampling without replacement which means that time series observations in each block have no duplicates. However, a crucial assumption to ensure that main statistical properties are not violated is the condition of exchangeable arrays; which is also the main challenging aspect when considering implementing a permutation-based testing approach to possibly nonstationary time series regression models.  


Consider the possibly nonstationary autoregressive model   

$$y_t = \beta_n y_{t-1} + u_t, \ \ \ t =  1,..., n .$$

where

$$ \beta_n = \left( 1 + \frac{ c }{ n^{\lambda} } \right), \ \ \lambda = 1 \ \text{or} \ \lambda \in (0,1) \ \ \text{and} \ \ c \in \mathbb{R}.$$

```R


```

## Permutation-Based Inference in Nonstationary Predictive Regressions

$$y_t = \beta_n x_{t-1} + u_t, \ \ \ t =  1,..., n .$$

such that 

$$ x_t = \rho_n x_{t-1} + v_t \ \ \ \text{and} \ \ \ \rho_n = \left( 1 + \frac{ c }{ n^{\lambda} } \right),$$

where 

$$\ \ \lambda = 1 \ \text{or} \ \lambda \in (0,1) \ \ \text{and} \ \ c \in \mathbb{R}.$$

```R


```

## Remarks:

1. This R package employs the novel IVX-P estimator proposed in the literature recently and aims to investigate the performance of the specific resampling method such as the permutation-based approach for robust statistical inference purposes in comparison to conventional method as well as the bootstrap-based approach. 

2. A second important aspect related to the permutation-based approach for hypothesis testing in possibly nonstationary autoregressive models such as the nonstationary predictive regression, is the estimation of the long-run variance which builds-up in the statistic under the null hypothesis. However, the self-normalized version of test statistics with fixed b asymptotics, where b is the bandwidth as a fraction of the sample size, allows to improve the size properties with some sacrifice on the power performance of the tests. 

3. The permutation-based approach allow us to consider an alternative solution to the block-bootstrap approach as an approximation to finite-sample distribution results - and critical values. Thus, we compare the performance of our testing procedure in relation to asymptotic results (via the nuisance-parameter free limiting distribution under the null hypothesis) for the permutation-based versus the block-bootstrap based approaches to obtain useful insights. On the other hand, a comparison of a studentized versus a self-normalized test statistic across these two resampling methods is not necessary because of various reasons, such as we know that the bootstrap versus the permutation based approach behaves differently when the long-run variance is estimated as well as due to the fact that in the case of nonstationary time series regression models, a self-normalized test statistic is both preferred and necessary to ensure that there is a Type I Error control across the spectrum of persistence properties. Lastly, due to the aforementioned reasons we expect that power differences in the case of the studentized versus the self-normalized versions of the test statistics might not be large or not even comparable if such differences exist. Our focus on observing the finite and large sample behaviour of the test statistics across the two resampling methods which can provide insights on how these two methods perform.   

4. Lastly our proposed methodology contributes to the literature in various directions such as the permutation-based approach when considering robust inference in nonstationary time series models, as well as in the statistics literature of resampling estimators. In particular, block-based resampling estimators have been intensively investigated for weakly dependent stochastic processes, however little is known about resampling performance and block sizes under strong or long-range dependence. Specifically, in the nonstationary time series econometrics literature, where nonstationarity is defined in terms of the local-to-unity specification which permits to incorporate near-integrated, near non-stationary and mildy explosive processes, the interest is on constructing robust estimation and inference methods regardless of the persistence properties of regressors.  

# Key References:

$\textbf{[1]}$ Katsouris, C. (2022e). "A permutation-based approach for Hypothesis Testing in Nonstationary Autoregressive Regressions". University of Exeter. Working paper. 

$\textbf{[2]}$ Katsouris, C. (2021e). "Bootstrapping Nonstationary Autoregressive Processes in Predictive Regression". University of Southampton. Working paper.

$\textbf{[3]}$ Katsouris, C. (2020). "Treatment effect validation via a permutation test in Stata". University of Southampton. Working paper.

$\textbf{[4]}$ Demetrescu, M., Georgiev, I., Rodrigues, P. M., & Taylor, A. R. (2022). "Extensions to IVX methods of inference for return predictability". Journal of Econometrics. 

$\textbf{[5]}$ Chan, K. W. (2022). "Optimal difference-based variance estimators in time series: A general framework". The Annals of Statistics, 50(3), 1376-1400.

$\textbf{[6]}$ Austern, M., & Orbanz, P. (2022). "Limit theorems for distributions invariant under groups of transformations". The Annals of Statistics, 50(4), 1960-1991.

$\textbf{[7]}$ Reichold, K., & Jentsch, C. (2022). A bootstrap-assisted self-normalization approach to inference in cointegrating regressions. arXiv preprint arXiv:2204.01373.

$\textbf{[8]}$  Kojevnikov, D., Marmer, V., & Song, K. (2021). Limit theorems for network dependent random variables. Journal of Econometrics, 222(2), 882-908.

$\textbf{[9]}$ Kojevnikov, D. (2021). "The bootstrap for network dependent processes". arXiv preprint arXiv:2101.12312.

$\textbf{[10]}$ Cavaliere, G., & Georgiev, I. (2020). "Inference under random limit bootstrap measures". Econometrica, 88(6), 2547-2574.

$\textbf{[11]}$ Kostakis, A., Magdalinos, T., & Stamatogiannis, M. P. (2015). "Robust econometric inference for stock return predictability". The Review of Financial Studies, 28(5), 1506-1553.

$\textbf{[12]}$ Shao, X. (2010). "The dependent wild bootstrap". Journal of the American Statistical Association, 105(489), 218-235.

$\textbf{[13]}$ Phillips, P. C., & Magdalinos, T. (2007). Limit theory for moderate deviations from a unit root. Journal of Econometrics, 136(1), 115-130.

$\textbf{[14]}$ Jansson, M., & Moreira, M. J. (2006). Optimal inference in regression models with nearly integrated regressors. Econometrica, 74(3), 681-714.

$\textbf{[15]}$ Andrews, D. W. (2004). "The block–block bootstrap: improved asymptotic refinements". Econometrica, 72(3), 673-700.

$\textbf{[16]}$  Paparoditis, E., & Politis, D. N. (2005). Bootstrapping unit root tests for autoregressive time series. Journal of the American Statistical Association, 100(470), 545-553.

$\textbf{[17]}$ Paparoditis, E., & Politis, D. N. (2003). "Residual‐based block bootstrap for unit root testing". Econometrica, 71(3), 813-855.

$\textbf{[18]}$ Gonçalves, S., & Kilian, L. (2004). Bootstrapping autoregressions with conditional heteroskedasticity of unknown form. Journal of econometrics, 123(1), 89-120.

$\textbf{[19]}$ Gonçalves, S., & White, H. (2002). The bootstrap of the mean for dependent heterogeneous arrays. Econometric Theory, 18(6), 1367-1384.

$\textbf{[20]}$ Penrose, M. D., & Yukich, J. E. (2003). Weak laws of large numbers in geometric probability. The Annals of Applied Probability, 13(1), 277-303.

$\textbf{[21]}$ Carlstein, E., Do, K. A., Hall, P., Hesterberg, T., & Künsch, H. R. (1998). "Matched-block bootstrap for dependent data". Bernoulli, 305-328.

$\textbf{[22]}$ Lahiri, S. N. (1999). "Theoretical comparisons of block bootstrap methods". Annals of Statistics, 386-404.

$\textbf{[23]}$  Elliott, G., Rothenberg, T.J., and Stock, J.H. (1996). Efficient tests for an autoregressive unit root. Econometrica, 64(4), 813-836.

$\textbf{[24]}$ Politis, D. N., & Romano, J. P. (1994). "The stationary bootstrap". Journal of the American Statistical association, 89(428), 1303-1313.


# Code of Coduct

Please note that the [‘PermLURM’](https://github.com/christiskatsouris/PermLURM) R project will be released with a Contributor Code of Coduct (under construction). By contributing to this project, you agree to abide by its terms.

# Acknowledgments

The author greatfully acknowledges financial support from the [Department of Economics](http://business-school.exeter.ac.uk/about/departments/economics/) of the [Faculty of Environment, Science and Economy](https://www.exeter.ac.uk/departments/ese/) at the University of Exeter, United Kingdom. 

Christis G. Katsouris is a Lecturer in Economics at the [University of Exeter Business School](http://business-school.exeter.ac.uk/). He is also a member of the [Time Series and Machine Learning Group](https://www.personal.soton.ac.uk/cz1y20/Reading_Group/mlts-group-2022.html) at the [School of Mathematical Sciences](https://www.southampton.ac.uk/about/faculties-schools-departments/school-of-mathematical-sciences) (Statistics Division) of the University of Southampton. 

# Declarations

The author (Christis G. Katsouris) declares no conflicts of interest.

Notice that the academic research presented here is considered to be as open access to the academic and non-academic community. Therefore, we would appreciate it if appropriate acknolwedgement is given to statistical methodologies and econometric procedures developed by academic researchers and made available to the wider applied data scientist community.   

# Historical Background

> Standing on the shoulders of giants.
> 
> $\textit{''If I have been able to see further, it was only because I stood on the shoulders of giants."}$
> $- \text{Isaac Newton, 1676}$ 
 
$\textbf{Raghu Raj Bahadur}$ (30 April 1924 – 7 June 1997) was an Indian statistician considered by peers to be "one of the architects of the modern theory of mathematical statistics". He received his doctorate from the University of North Carolina under Herbert Robbins in 1950 after which he joined University of Chicago. He worked as a research statistician at the Indian Statistical Institute in Calcutta from 1956 to 1961. Bahadur spent the remainder of his academic career in the University of Chicago. He published numerous papers and is best known for the concepts of "Bahadur efficiency" and the Bahadur–Ghosh–Kiefer representation (with J. K. Ghosh and Jack Kiefer). Bahadur also framed the Anderson–Bahadur algorithm[9] along with Theodore Wilbur Anderson which is used in statistics and engineering for solving binary classification problems when the underlying data have multivariate normal distributions with different covariance matrices (Source: Wikipedia).  

# How to Cite a Website

See: https://www.mendeley.com/guides/web-citation-guide/
