**I. Introduction to Probability**

*   Understanding Basic Probability Concepts
    *   Defining sample spaces and events
    *   Calculating probabilities: classical, empirical, subjective
    *   Understanding set theory relevant to probability (union, intersection, complement)
*   Axioms of Probability
    *   Non-negativity axiom: P(A) ≥ 0
    *   Additivity axiom: P(A∪B) = P(A) + P(B) if A and B are mutually exclusive
    *   Normalization axiom: P(S) = 1, where S is the sample space
*   Conditional Probability
    *   Defining conditional probability: P(A|B) = P(A∩B) / P(B)
    *   Understanding and applying Bayes' Theorem: P(A|B) = [P(B|A) * P(A)] / P(B)
    *   Applications of conditional probability in real-world scenarios (e.g., medical testing)

**II. Random Variables and Distributions**

*   Discrete Random Variables
    *   Defining discrete random variables
    *   Understanding probability mass functions (PMF)
    *   Common discrete distributions:
        *   Bernoulli distribution: `P(X=x) = p^x (1-p)^(1-x)` for x = 0, 1
        *   Binomial distribution: `P(X=k) = (n choose k) * p^k * (1-p)^(n-k)`
        *   Poisson distribution: `P(X=k) = (λ^k * e^(-λ)) / k!`
*   Continuous Random Variables
    *   Defining continuous random variables
    *   Understanding probability density functions (PDF)
    *   Cumulative distribution function (CDF): `F(x) = P(X ≤ x)`
    *   Common continuous distributions:
        *   Uniform distribution: `f(x) = 1/(b-a)` for a ≤ x ≤ b
        *   Exponential distribution: `f(x) = λ * e^(-λx)` for x ≥ 0
        *   Normal (Gaussian) distribution: `f(x) = (1 / (σ * sqrt(2π))) * e^(-((x-μ)^2) / (2σ^2))`
*   Expected Value and Variance
    *   Calculating the expected value of a discrete random variable: `E[X] = Σ x * P(X=x)`
    *   Calculating the expected value of a continuous random variable: `E[X] = ∫ x * f(x) dx`
    *   Calculating variance: `Var(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2`
    *   Understanding standard deviation: `SD(X) = sqrt(Var(X))`

**III. Joint Distributions and Independence**

*   Joint Probability Distributions
    *   Understanding joint PMFs and PDFs for multiple random variables
    *   Marginal distributions: deriving the distribution of a single variable from a joint distribution
    *   Conditional distributions: `P(X=x | Y=y) = P(X=x, Y=y) / P(Y=y)`
*   Independence of Random Variables
    *   Defining independence: `P(X=x, Y=y) = P(X=x) * P(Y=y)` for all x and y
    *   Testing for independence using joint and marginal distributions
*   Covariance and Correlation
    *   Calculating covariance: `Cov(X, Y) = E[(X - E[X]) * (Y - E[Y])]`
    *   Calculating correlation: `Corr(X, Y) = Cov(X, Y) / (SD(X) * SD(Y))`
    *   Interpreting covariance and correlation values: positive, negative, zero correlation

**IV. Limit Theorems**

*   Markov's Inequality
    *   Understanding Markov's inequality: `P(X ≥ a) ≤ E[X] / a` for a non-negative random variable X and a > 0
*   Chebyshev's Inequality
    *   Understanding Chebyshev's inequality: `P(|X - E[X]| ≥ k) ≤ Var(X) / k^2`
*   Law of Large Numbers (LLN)
    *   Weak Law of Large Numbers (WLLN)
    *   Strong Law of Large Numbers (SLLN)
    *   Applications of the LLN: sample means converging to the population mean
*   Central Limit Theorem (CLT)
    *   Understanding the CLT: the distribution of the sample mean approaches a normal distribution as the sample size increases
    *   Applications of the CLT in statistical inference

**V. Statistical Inference**

*   Estimation
    *   Point estimation: estimating a parameter using a single value
        *   Maximum Likelihood Estimation (MLE)
        *   Method of Moments
    *   Interval estimation: constructing confidence intervals
        *   Confidence intervals for the mean (known and unknown variance)
        *   Confidence intervals for proportions
*   Hypothesis Testing
    *   Null and alternative hypotheses
    *   Type I and Type II errors
    *   Significance level (alpha) and p-value
    *   One-tailed and two-tailed tests
    *   Common hypothesis tests:
        *   z-tests
        *   t-tests
        *   Chi-squared tests
*   Regression Analysis
    *   Linear Regression
        *   Simple linear regression model: `y = β₀ + β₁x + ε`
        *   Estimating regression coefficients (β₀ and β₁)
        *   Interpreting regression coefficients
        *   Assessing model fit (R-squared)
    *   Multiple Linear Regression
        *   Extending linear regression to multiple predictors
        *   Understanding multicollinearity
        *   Variable selection techniques (e.g., stepwise regression)
