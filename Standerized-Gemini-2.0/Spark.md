**I. Introduction to Probability**

*   Understanding Basic Concepts
    *   Defining sample space, events, and outcomes
    *   Differentiating between discrete and continuous random variables
*   Axioms of Probability
    *   Probability of an event: 0 ≤ P(A) ≤ 1
    *   Probability of the sample space: P(S) = 1
    *   Probability of mutually exclusive events: P(A ∪ B) = P(A) + P(B)
*   Calculating Probabilities
    *   Using counting techniques (permutations and combinations)
        *   Example: Calculating the probability of drawing specific cards from a deck.
    *   Applying the addition rule: P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
    *   Applying the complement rule: P(A') = 1 - P(A)

**II. Conditional Probability and Independence**

*   Understanding Conditional Probability
    *   Defining conditional probability: P(A|B) = P(A ∩ B) / P(B)
    *   Calculating conditional probabilities from given data
        *   Example: Determining the probability of a disease given a positive test result.
*   Bayes' Theorem
    *   Applying Bayes' Theorem: P(A|B) = [P(B|A) * P(A)] / P(B)
    *   Solving problems using Bayes' Theorem
        *   Example: Medical diagnosis, spam filtering
*   Understanding Independence
    *   Defining independent events: P(A ∩ B) = P(A) * P(B)
    *   Determining if events are independent
        *   Example: Coin flips, rolling dice

**III. Discrete Random Variables**

*   Probability Mass Functions (PMF)
    *   Defining a PMF: P(X = x)
    *   Verifying if a function is a valid PMF
*   Common Discrete Distributions
    *   Bernoulli Distribution
        *   Understanding parameters and applications
        *   Example: Modeling a single trial with binary outcome (success/failure)
    *   Binomial Distribution
        *   Understanding parameters (n, p) and applications
        *   Calculating probabilities using the binomial formula: P(X = k) = (n choose k) * p^k * (1-p)^(n-k)
        *   Example: Number of successes in a fixed number of independent trials.
    *   Poisson Distribution
        *   Understanding the parameter (λ) and applications
        *   Calculating probabilities using the Poisson formula: P(X = k) = (λ^k * e^(-λ)) / k!
        *   Example: Number of events occurring in a fixed interval of time or space.
*   Expected Value and Variance
    *   Calculating the expected value: E[X] = Σ [x * P(X = x)]
    *   Calculating the variance: Var(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2
    *   Applying these concepts to specific discrete distributions

**IV. Continuous Random Variables**

*   Probability Density Functions (PDF)
    *   Defining a PDF: f(x)
    *   Understanding the relationship between PDF and cumulative distribution function (CDF): F(x) = ∫ -∞ to x f(t) dt
    *   Verifying if a function is a valid PDF: ∫ -∞ to ∞ f(x) dx = 1
*   Common Continuous Distributions
    *   Uniform Distribution
        *   Understanding parameters (a, b) and applications
        *   Calculating probabilities and percentiles.
    *   Exponential Distribution
        *   Understanding the parameter (λ) and applications
        *   Applications to waiting times and reliability.
    *   Normal Distribution
        *   Understanding parameters (μ, σ) and applications
        *   Using the standard normal distribution (Z) and Z-tables.
        *   Applying the central limit theorem (CLT).
*   Expected Value and Variance
    *   Calculating the expected value: E[X] = ∫ -∞ to ∞ x * f(x) dx
    *   Calculating the variance: Var(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2
    *   Applying these concepts to specific continuous distributions

**V. Joint Distributions**

*   Understanding Joint PMFs and PDFs
    *   Defining joint probability mass functions (PMFs) for discrete variables.
        *   Example: P(X = x, Y = y)
    *   Defining joint probability density functions (PDFs) for continuous variables.
        *   Example: f(x, y)
*   Marginal Distributions
    *   Deriving marginal PMFs from joint PMFs: P(X = x) = Σy P(X = x, Y = y)
    *   Deriving marginal PDFs from joint PDFs: fX(x) = ∫ -∞ to ∞ f(x, y) dy
*   Conditional Distributions
    *   Defining conditional PMFs: P(X = x | Y = y) = P(X = x, Y = y) / P(Y = y)
    *   Defining conditional PDFs: f(x | y) = f(x, y) / fY(y)
*   Independence of Random Variables
    *   Defining independent random variables: f(x, y) = fX(x) * fY(y)
*   Covariance and Correlation
    *   Calculating covariance: Cov(X, Y) = E[(X - E[X])(Y - E[Y])] = E[XY] - E[X]E[Y]
    *   Calculating correlation: Corr(X, Y) = Cov(X, Y) / (σX * σY)
    *   Interpreting covariance and correlation.

**VI. Sampling Distributions and the Central Limit Theorem**

*   Understanding Sampling Distributions
    *   Defining a sampling distribution of a statistic
    *   Calculating the mean and standard deviation of a sampling distribution
        *   Example: Distribution of the sample mean, sample variance.
*   The Central Limit Theorem (CLT)
    *   Understanding the CLT: The distribution of the sample mean approaches a normal distribution as the sample size increases.
    *   Applying the CLT to solve problems
        *   Example: Estimating population parameters using sample statistics.
*   Confidence Intervals
    *   Constructing confidence intervals for the population mean
        *   Using the Z-distribution when the population standard deviation is known.
        *   Using the t-distribution when the population standard deviation is unknown.
    *   Constructing confidence intervals for the population proportion.
*   Hypothesis Testing
    *   Formulating null and alternative hypotheses.
    *   Choosing a significance level (α).
    *   Calculating test statistics (Z-statistic, t-statistic).
    *   Determining p-values.
    *   Making decisions based on the p-value and significance level.

**VII. Advanced Topics (Optional)**

*   Markov Chains
    *   Understanding states, transition probabilities, and state diagrams.
    *   Calculating stationary distributions.
*   Monte Carlo Methods
    *   Using simulation to estimate probabilities and expectations.
*   Information Theory
    *   Understanding entropy, information gain, and Kullback-Leibler divergence.
*   Bayesian Inference
    *   Updating prior beliefs based on observed data.
