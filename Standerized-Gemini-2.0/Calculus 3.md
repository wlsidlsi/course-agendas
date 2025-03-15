**I. Vector Algebra and Geometry**

*   Understanding 3D Coordinate Systems
    *   Right-hand rule
    *   Distance formula in 3D: `√((x₂ - x₁)² + (y₂ - y₁)² + (z₂ - z₁)²) `

*   Vectors in 3D Space
    *   Vector components and representation: `<a, b, c>`
    *   Vector addition and scalar multiplication
    *   Unit vectors: `i = <1, 0, 0>`, `j = <0, 1, 0>`, `k = <0, 0, 1>`

*   Dot Product
    *   Calculating the dot product: `a · b = |a| |b| cos θ`
    *   Applications: Finding the angle between vectors, checking for orthogonality

*   Cross Product
    *   Calculating the cross product: `a x b = <a₂b₃ - a₃b₂, a₃b₁ - a₁b₃, a₁b₂ - a₂b₁>`
    *   Applications: Finding a vector perpendicular to two given vectors, calculating area of a parallelogram

*   Equations of Lines and Planes
    *   Parametric equations of a line: `r(t) = r₀ + tv`
    *   Equation of a plane: `ax + by + cz = d`

**II. Vector-Valued Functions**

*   Understanding Vector-Valued Functions
    *   Representing curves in 3D space: `r(t) = <f(t), g(t), h(t)>`
    *   Domain and range of vector-valued functions

*   Calculus of Vector-Valued Functions
    *   Limits and continuity
    *   Derivatives: `r'(t) = <f'(t), g'(t), h'(t)>`
    *   Integrals: `∫ r(t) dt = <∫ f(t) dt, ∫ g(t) dt, ∫ h(t) dt>`

*   Arc Length and Curvature
    *   Arc length parameterization: `s(t) = ∫ |r'(u)| du` from `a` to `t`
    *   Curvature: `κ(t) = |T'(t)| / |r'(t)|` where `T(t) = r'(t) / |r'(t)|` (unit tangent vector)

*   Tangential and Normal Components of Acceleration
    *   Tangential component: `a_T = v'(t)` where `v(t) = |r'(t)|` (speed)
    *   Normal component: `a_N = κ(t) (v(t))²`
    *   Acceleration vector decomposition: `a = a_T T + a_N N`

**III. Multivariable Functions**

*   Understanding Multivariable Functions
    *   Functions of two variables: `z = f(x, y)`
    *   Functions of three variables: `w = f(x, y, z)`
    *   Domain and range of multivariable functions

*   Limits and Continuity
    *   Evaluating limits of multivariable functions
    *   Understanding the concept of continuity in multiple dimensions

*   Partial Derivatives
    *   First-order partial derivatives: `∂f/∂x`, `∂f/∂y`
    *   Second-order partial derivatives: `∂²f/∂x²`, `∂²f/∂y²`, `∂²f/∂x∂y`, `∂²f/∂y∂x`
    *   Clairaut's Theorem: `∂²f/∂x∂y = ∂²f/∂y∂x` under certain conditions

*   Tangent Planes and Linear Approximations
    *   Equation of the tangent plane: `z - z₀ = fₓ(x₀, y₀)(x - x₀) + fᵧ(x₀, y₀)(y - y₀)`
    *   Linear approximation: `f(x, y) ≈ f(x₀, y₀) + fₓ(x₀, y₀)(x - x₀) + fᵧ(x₀, y₀)(y - y₀)`

*   Chain Rule
    *   Chain rule for one independent variable: `dz/dt = (∂z/∂x)(dx/dt) + (∂z/∂y)(dy/dt)`
    *   Chain rule for multiple independent variables

*   Directional Derivatives and the Gradient
    *   Directional derivative: `Dᵤf(x, y) = ∇f(x, y) · u` where `u` is a unit vector
    *   Gradient vector: `∇f(x, y) = <∂f/∂x, ∂f/∂y>`
    *   Maximum rate of change and direction

*   Optimization
    *   Finding critical points: `∇f(x, y) = <0, 0>`
    *   Second derivative test for local extrema: using the discriminant `D = fₓₓfᵧᵧ - (fₓᵧ)²`
    *   Absolute extrema on a closed region

*   Lagrange Multipliers
    *   Constrained optimization problems: `maximize/minimize f(x, y) subject to g(x, y) = k`
    *   Solving the system of equations: `∇f(x, y) = λ∇g(x, y)` and `g(x, y) = k`

**IV. Multiple Integrals**

*   Double Integrals over Rectangles
    *   Definition of the double integral
    *   Fubini's Theorem: `∬R f(x, y) dA = ∫a to b ∫c to d f(x, y) dy dx = ∫c to d ∫a to b f(x, y) dx dy`

*   Double Integrals over General Regions
    *   Type I regions: `D = {(x, y) | a ≤ x ≤ b, g₁(x) ≤ y ≤ g₂(x)}`
    *   Type II regions: `D = {(x, y) | c ≤ y ≤ d, h₁(y) ≤ x ≤ h₂(y)}`
    *   Setting up and evaluating double integrals

*   Double Integrals in Polar Coordinates
    *   Coordinate transformation: `x = r cos θ`, `y = r sin θ`
    *   Jacobian: `dA = r dr dθ`
    *   Evaluating integrals in polar coordinates

*   Applications of Double Integrals
    *   Area: `A = ∬D dA`
    *   Volume: `V = ∬D f(x, y) dA`
    *   Mass and center of mass: `m = ∬D ρ(x, y) dA`, `(x̄, ȳ)`

*   Triple Integrals
    *   Triple integrals in rectangular coordinates
    *   Triple integrals in cylindrical coordinates: `x = r cos θ`, `y = r sin θ`, `z = z`, `dV = r dz dr dθ`
    *   Triple integrals in spherical coordinates: `x = ρ sin φ cos θ`, `y = ρ sin φ sin θ`, `z = ρ cos φ`, `dV = ρ² sin φ dρ dφ dθ`

*   Change of Variables in Multiple Integrals
    *   Jacobian determinant for transformations: `∂(x, y) / ∂(u, v)`
    *   Transforming regions of integration

**V. Vector Calculus**

*   Vector Fields
    *   Understanding vector fields in 2D and 3D
    *   Gradient vector fields: `F = ∇f`

*   Line Integrals
    *   Line integrals of scalar functions: `∫C f(x, y, z) ds`
    *   Line integrals of vector fields: `∫C F · dr`
    *   Fundamental Theorem for Line Integrals: `∫C ∇f · dr = f(r(b)) - f(r(a))`

*   Conservative Vector Fields
    *   Checking for conservative vector fields: `∂P/∂y = ∂Q/∂x` (in 2D) or `curl F = 0` (in 3D)
    *   Finding potential functions

*   Green's Theorem
    *   Relating line integrals to double integrals: `∮C P dx + Q dy = ∬D (∂Q/∂x - ∂P/∂y) dA`

*   Surface Integrals
    *   Parametric surfaces: `r(u, v) = <x(u, v), y(u, v), z(u, v)>`
    *   Surface integrals of scalar functions: `∬S f(x, y, z) dS`
    *   Surface integrals of vector fields: `∬S F · dS`

*   Divergence and Curl
    *   Divergence: `div F = ∇ · F = ∂P/∂x + ∂Q/∂y + ∂R/∂z`
    *   Curl: `curl F = ∇ x F = <∂R/∂y - ∂Q/∂z, ∂P/∂z - ∂R/∂x, ∂Q/∂x - ∂P/∂y>`

*   Stokes' Theorem
    *   Relating surface integrals to line integrals: `∮C F · dr = ∬S (curl F) · dS`

*   Divergence Theorem
    *   Relating surface integrals to triple integrals: `∬S F · dS = ∭E (div F) dV`
