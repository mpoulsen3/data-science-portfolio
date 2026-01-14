# Data Science Portfolio

This repository contains selected projects illustrating work from my Master’s in Data Science program,
as well as related applied projects. The focus is on statistical modeling, uncertainty quantification,
and translating complex model outputs into interpretable insights.

## Projects

### Project 1: COVID-19 Modeling and Prediction Under Uncertainty
[View Project](COVID19_SEIR/README.md)

**Problem**

Epidemiological models are inherently uncertain due to noisy data, incomplete knowledge of system
dynamics, and model discrepancy. This project examines how different calibration and uncertainty
propagation techniques affect predictive confidence and interpretability when modeling COVID-19 data.

**Data**

The data used in this project comes from the Kaggle *COVID-19 Global Forecasting (Week 5)* competition.
The dataset includes daily, country- and region-level time series of confirmed cases and fatalities,
along with associated metadata. In this project, the data is aggregated to overall U.S. case counts in
order to focus on uncertainty quantification and modeling behavior, while retaining real-world
challenges such as cyclical reporting delays.

**Approach**

An SEIR compartmental model is used to describe COVID-19 dynamics, with parameters governing infection,
latency, recovery, fatality rates, and time-varying transmission behavior. Model calibration and
prediction are performed using both frequentist and Bayesian uncertainty quantification techniques.

Key methodological components include:
- Deterministic SEIR modeling using ordinary differential equations
- Parameter estimation via frequentist optimization (ordinary least squares)
- Construction of frequentist prediction intervals based on calibrated model uncertainty
- Bayesian parameter calibration using Delayed Rejection Adaptive Metropolis (DRAM) MCMC
- Posterior analysis of parameter distributions and correlations
- Posterior predictive and credible intervals computed using `mcmcpred`
- Comparison of frequentist and Bayesian uncertainty representations

**Results**

The results demonstrate how uncertainty in epidemiological model parameters propagates into predictions
of infections and fatalities. Sensitivity to transmission and fatality parameters is quantified, and
frequentist prediction intervals are compared against Bayesian credible and posterior predictive
intervals. The analysis highlights meaningful differences in uncertainty characterization between the
two approaches, particularly in forward projections.

**Tools**

MATLAB, MCMC Toolbox for MATLAB
(Methods transferable to Python-based Bayesian frameworks)
