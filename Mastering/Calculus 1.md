**I. Limits and Continuity**

*   Understanding Limits Graphically and Numerically
    *   Estimating limits from graphs
    *   Using tables to estimate limits
*   Evaluating Limits Algebraically
    *   Direct substitution
    *   Factoring techniques
        *   Example: `lim (x->2) (x^2 - 4) / (x - 2)`
    *   Rationalizing techniques
        *   Example: `lim (x->0) (sqrt(x+1) - 1) / x`
*   One-Sided Limits and Infinite Limits
    *   Definition of one-sided limits
    *   Limits approaching infinity and at infinity
    *   Vertical and horizontal asymptotes
        *   Relating asymptotes to limits: `lim (x->c) f(x) = ±∞` implies vertical asymptote at `x=c`.
*   Continuity
    *   Definition of continuity at a point
    *   Types of discontinuities: removable, jump, infinite
    *   Intermediate Value Theorem
        *   Applying the IVT to show existence of roots

**II. Derivatives**

*   Definition of the Derivative
    *   The limit definition: `f'(x) = lim (h->0) (f(x+h) - f(x)) / h`
    *   Tangent lines and rates of change
*   Basic Differentiation Rules
    *   Power rule: `d/dx (x^n) = n*x^(n-1)`
    *   Constant multiple rule
    *   Sum and difference rules
    *   Derivatives of trigonometric functions
        *   `d/dx (sin(x)) = cos(x)`, `d/dx (cos(x)) = -sin(x)`
*   Product and Quotient Rules
    *   Product rule: `d/dx (u*v) = u'*v + u*v'`
    *   Quotient rule: `d/dx (u/v) = (u'*v - u*v') / v^2`
*   Chain Rule
    *   Applying the chain rule: `d/dx (f(g(x))) = f'(g(x)) * g'(x)`
    *   Derivatives of composite functions
*   Implicit Differentiation
    *   Differentiating equations implicitly
    *   Finding `dy/dx` when `y` is not explicitly defined in terms of `x`
    *   Example: Differentiating `x^2 + y^2 = 25` implicitly.
*   Higher-Order Derivatives
    *   Finding second, third, and higher derivatives
    *   Notation: `f''(x)`, `f'''(x)`, `d^2y/dx^2`

**III. Applications of Derivatives**

*   Related Rates
    *   Setting up and solving related rates problems
    *   Examples: Filling a cone with water, ladder sliding down a wall
*   Optimization
    *   Finding absolute and local extrema
    *   First and second derivative tests
    *   Optimization problems in various contexts
        *   Example: Maximizing the area of a rectangle with fixed perimeter.
*   Mean Value Theorem
    *   Understanding and applying the Mean Value Theorem
    *   Consequences of the Mean Value Theorem
*   Curve Sketching
    *   Using derivatives to analyze functions
    *   Finding intervals of increasing/decreasing
    *   Finding intervals of concavity and inflection points
    *   Sketching graphs of functions

**IV. Integration**

*   Antiderivatives and Indefinite Integrals
    *   Definition of an antiderivative
    *   Indefinite integral notation: `∫ f(x) dx = F(x) + C`
    *   Basic integration rules
        *   Power rule for integration: `∫ x^n dx = (x^(n+1))/(n+1) + C`
    *   Integrals of trigonometric functions
*   Definite Integrals
    *   Riemann sums and the definition of the definite integral
    *   The Fundamental Theorem of Calculus (FTC)
        *   FTC Part 1: `d/dx ∫[a to x] f(t) dt = f(x)`
        *   FTC Part 2: `∫[a to b] f(x) dx = F(b) - F(a)`
*   Substitution Rule (u-Substitution)
    *   Applying u-substitution to evaluate integrals
    *   Changing limits of integration when using definite integrals
    *   Example: `∫ 2x * cos(x^2) dx`
*   Applications of Integration
    *   Finding areas between curves
    *   Volumes of solids of revolution (disk/washer method, cylindrical shells)
    *   Average value of a function
        *   Formula: `f_avg = (1/(b-a)) ∫[a to b] f(x) dx`

**V. Advanced Integration Techniques (Optional for Calculus 1)**

*   Integration by Parts
    *   Using integration by parts: `∫ u dv = uv - ∫ v du`
    *   Choosing appropriate `u` and `dv`
*   Trigonometric Integrals
    *   Integrating powers of sine, cosine, tangent, and secant
*   Partial Fraction Decomposition
    *   Integrating rational functions using partial fractions
