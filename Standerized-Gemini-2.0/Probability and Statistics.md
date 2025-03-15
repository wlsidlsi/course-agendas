**I. Descriptive Statistics**

*   Understanding Data Types
    *   Categorical (Nominal, Ordinal)
    *   Numerical (Discrete, Continuous)
*   Measures of Central Tendency
    *   Calculating Mean: `sum(data) / len(data)`
    *   Finding Median: Middle value when data is sorted
    *   Determining Mode: Most frequent value
*   Measures of Dispersion
    *   Calculating Range: `max(data) - min(data)`
    *   Variance: Average of squared differences from the mean: `sum((x - mean)**2) / (n-1)`
    *   Standard Deviation: Square root of variance: `sqrt(variance)`
*   Data Visualization
    *   Histograms: Visualizing distribution of numerical data
    *   Box Plots: Displaying quartiles and outliers
    *   Scatter Plots: Showing relationship between two variables

**II. Probability Theory**

*   Basic Probability Concepts
    *   Defining Sample Space and Events
    *   Calculating Probability: `P(A) = Number of favorable outcomes / Total number of outcomes`
*   Conditional Probability
    *   Understanding conditional probability: `P(A|B) = P(A and B) / P(B)`
    *   Bayes' Theorem: `P(A|B) = (P(B|A) * P(A)) / P(B)`
*   Probability Distributions
    *   Discrete Distributions
        *   Bernoulli Distribution: Single trial with success/failure
        *   Binomial Distribution: Number of successes in fixed trials
        *   Poisson Distribution: Number of events in a fixed interval
    *   Continuous Distributions
        *   Normal Distribution: Bell-shaped curve, characterized by mean and standard deviation
        *   Exponential Distribution: Time until an event occurs
        *   Uniform Distribution: Equal probability over a range

**III. Inferential Statistics**

*   Sampling Distributions
    *   Central Limit Theorem: Distribution of sample means approaches normal distribution as sample size increases.
    *   Standard Error: Standard deviation of the sampling distribution of a statistic.
*   Hypothesis Testing
    *   Formulating Null and Alternative Hypotheses
    *   Choosing Significance Level (alpha)
    *   Performing Z-tests and T-tests
        *   Z-test: Using Z-statistic when population standard deviation is known.
        *   T-test: Using T-statistic when population standard deviation is unknown.
    *   Calculating P-value: Probability of observing the test statistic under the null hypothesis.
    *   Making Decisions: Reject or fail to reject the null hypothesis.
*   Confidence Intervals
    *   Calculating confidence intervals for population mean and proportion
    *   Interpreting confidence intervals
*   Regression Analysis
    *   Simple Linear Regression: Modeling relationship between two variables: `y = mx + b`
    *   Multiple Linear Regression: Modeling relationship between multiple variables.
    *   Evaluating Model Fit: R-squared, adjusted R-squared

**IV. Advanced Topics**

*   Analysis of Variance (ANOVA)
    *   One-way ANOVA: Comparing means of multiple groups.
    *   Two-way ANOVA: Examining the effect of two independent variables on a dependent variable.
*   Non-parametric Tests
    *   Chi-square test: Testing independence of categorical variables.
    *   Mann-Whitney U test: Comparing two independent samples when data is not normally distributed.
    *   Kruskal-Wallis test: Comparing multiple independent samples when data is not normally distributed.
*   Time Series Analysis
    *   Understanding time series data
    *   Decomposing time series data into trend, seasonality, and residuals
    *   Forecasting techniques: Moving Averages, Exponential Smoothing, ARIMA models
*   Machine Learning Applications
    *   Classification Algorithms: Logistic Regression, Support Vector Machines, Decision Trees
    *   Clustering Algorithms: K-Means, Hierarchical Clustering
