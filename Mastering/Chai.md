**I. Introduction to Probability**

*   Understanding Basic Probability Concepts
    *   Defining sample space, events, and outcomes
    *   Calculating probabilities using classical, empirical, and subjective methods
    *   Examples: Coin flips, dice rolls, card draws
*   Exploring Set Theory and Probability
    *   Understanding set operations: union, intersection, complement
    *   Applying set theory to calculate probabilities of combined events
    *   Using Venn diagrams to visualize probabilities
*   Conditional Probability
    *   Defining conditional probability and its formula: P(A|B) = P(A ∩ B) / P(B)
    *   Understanding independence of events: P(A|B) = P(A)
    *   Applying Bayes' Theorem: P(A|B) = [P(B|A) * P(A)] / P(B)
    *   Example: Medical testing scenarios

**II. Random Variables and Distributions**

*   Discrete Random Variables
    *   Defining discrete random variables and probability mass functions (PMFs)
    *   Understanding and applying the Bernoulli distribution
    *   Understanding and applying the Binomial distribution
        *   Calculating probabilities: `P(X = k) = (n choose k) * p^k * (1-p)^(n-k)`
    *   Understanding and applying the Poisson distribution
        *   Calculating probabilities: `P(X = k) = (λ^k * e^(-λ)) / k!`
    *   Calculating expected value and variance of discrete random variables
*   Continuous Random Variables
    *   Defining continuous random variables and probability density functions (PDFs)
    *   Understanding and applying the Uniform distribution
    *   Understanding and applying the Exponential distribution
    *   Understanding and applying the Normal distribution
        *   Standard Normal Distribution (Z-distribution) and its properties
        *   Converting to Z-scores: `z = (x - μ) / σ`
    *   Calculating expected value and variance of continuous random variables
*   Cumulative Distribution Functions (CDFs)
    *   Understanding the definition and properties of CDFs
    *   Calculating probabilities using CDFs for both discrete and continuous variables
    *   Relating CDFs to PMFs and PDFs

**III. Joint Distributions and Independence**

*   Joint Probability Distributions
    *   Defining joint PMFs and PDFs for multiple random variables
    *   Calculating marginal distributions from joint distributions
    *   Understanding conditional distributions
*   Independence of Random Variables
    *   Defining independence of random variables: `P(X, Y) = P(X) * P(Y)`
    *   Calculating covariance and correlation to assess dependence
    *   Understanding the properties of independent random variables
*   Functions of Random Variables
    *   Determining the distribution of a function of a single random variable
    *   Determining the distribution of a function of multiple random variables
    *   Example: Sum of independent random variables

**IV. Statistical Inference**

*   Sampling Distributions
    *   Understanding the concept of a sampling distribution
    *   Describing the sampling distribution of the sample mean
        *   Central Limit Theorem (CLT)
    *   Describing the sampling distribution of the sample proportion
*   Estimation
    *   Point Estimation
        *   Understanding bias and variance of estimators
        *   Calculating point estimates for population parameters (mean, variance, proportion)
    *   Interval Estimation
        *   Constructing confidence intervals for population mean (using t-distribution when σ is unknown)
        *   Constructing confidence intervals for population proportion
        *   Factors affecting confidence interval width: sample size, confidence level, standard deviation
*   Hypothesis Testing
    *   Formulating null and alternative hypotheses
    *   Understanding Type I and Type II errors
    *   Performing hypothesis tests for population mean (t-tests and z-tests)
    *   Performing hypothesis tests for population proportion (z-tests)
    *   Calculating p-values and interpreting their significance
    *   Example: Testing if the average height of students is 5'8"

**V. Regression Analysis**

*   Simple Linear Regression
    *   Understanding the linear regression model: `y = β0 + β1x + ε`
    *   Estimating regression coefficients using least squares method
    *   Assessing the goodness of fit: R-squared
    *   Performing hypothesis tests on regression coefficients
    *   Constructing confidence intervals for regression coefficients
    *   Making predictions using the regression model
*   Multiple Linear Regression
    *   Extending the linear regression model to multiple predictors: `y = β0 + β1x1 + β2x2 + ... + ε`
    *   Interpreting regression coefficients in multiple regression
    *   Addressing multicollinearity
    *   Model selection techniques (e.g., forward selection, backward elimination)
*   Regression Diagnostics
    *   Checking for linearity, independence, homoscedasticity, and normality of residuals
    *   Identifying outliers and influential observations
    *   Transforming variables to improve model fit

**VI. Bayesian Statistics (Introduction)**

*   Bayes' Theorem Revisited
    *   Understanding the Bayesian interpretation of probability
    *   Applying Bayes' Theorem to update beliefs based on evidence
*   Prior, Likelihood, and Posterior Distributions
    *   Defining prior, likelihood, and posterior distributions
    *   Choosing appropriate prior distributions (e.g., conjugate priors)
    *   Calculating the posterior distribution
*   Bayesian Inference
    *   Estimating parameters using Bayesian methods
    *   Constructing credible intervals (Bayesian confidence intervals)
    *   Comparing Bayesian and frequentist approaches to inference
*   Example: Bayesian A/B Testing
