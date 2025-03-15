**I. Introduction to Reinforcement Learning (RL)**

*   Understanding the RL framework
    *   Agents, environments, states, actions, rewards, policies
    *   Markov Decision Processes (MDPs) as the formal basis
*   Distinguishing RL from other machine learning paradigms
    *   Supervised learning (labeled data) vs. RL (trial and error)
    *   Unsupervised learning (finding patterns) vs. RL (optimizing behavior)
*   Applications of RL
    *   Game playing (e.g., AlphaGo)
    *   Robotics (e.g., robot navigation)
    *   Resource management (e.g., optimizing energy consumption)

**II. Markov Decision Processes (MDPs)**

*   Formal definition of MDPs
    *   States (S), Actions (A), Transition function (P), Reward function (R), Discount factor (γ)
    *   Understanding state transitions: `P(s'|s, a)` - probability of transitioning to state s' from state s after taking action a
    *   Defining the reward function: `R(s, a, s')` - reward received after transitioning from state s to s' by taking action a.
*   Policies and Value Functions
    *   Policy (π): A mapping from states to actions: `π(a|s)` - probability of taking action a in state s
    *   State-value function (V): Expected return starting from a state s following policy π: `Vπ(s) = Eπ[Gt|St=s]`
    *   Action-value function (Q): Expected return starting from a state s, taking action a, and then following policy π: `Qπ(s, a) = Eπ[Gt|St=s, At=a]`
*   Bellman Equations
    *   Bellman equation for V(s): `Vπ(s) = Σa π(a|s) Σs' P(s'|s, a) [R(s, a, s') + γ Vπ(s')]`
    *   Bellman equation for Q(s, a): `Qπ(s, a) = Σs' P(s'|s, a) [R(s, a, s') + γ Σa' π(a'|s') Qπ(s', a')]`
*   Optimal Policies and Value Functions
    *   Optimal state-value function: `V*(s) = maxπ Vπ(s)`
    *   Optimal action-value function: `Q*(s, a) = maxπ Qπ(s, a)`
    *   Bellman optimality equations:
        *   `V*(s) = maxa Σs' P(s'|s, a) [R(s, a, s') + γ V*(s')]`
        *   `Q*(s, a) = Σs' P(s'|s, a) [R(s, a, s') + γ maxa' Q*(s', a')]`

**III. Dynamic Programming (DP) for RL**

*   Policy Evaluation (Prediction)
    *   Iteratively computing the state-value function Vπ for a given policy π
    *   Using the Bellman equation for Vπ in an iterative update: `Vk+1(s) = Σa π(a|s) Σs' P(s'|s, a) [R(s, a, s') + γ Vk(s')]`
*   Policy Improvement
    *   Improving a policy π to π' by acting greedily with respect to Vπ
    *   `π'(s) = argmaxa Σs' P(s'|s, a) [R(s, a, s') + γ Vπ(s')]`
*   Policy Iteration
    *   Iteratively performing policy evaluation and policy improvement until convergence to an optimal policy.
    *   Guaranteed convergence to the optimal policy π*
*   Value Iteration
    *   Iteratively computing the optimal state-value function V* directly
    *   Using the Bellman optimality equation for V* in an iterative update: `Vk+1(s) = maxa Σs' P(s'|s, a) [R(s, a, s') + γ Vk(s')]`
    *   One-step lookahead search

**IV. Monte Carlo Methods**

*   Monte Carlo Prediction (Policy Evaluation)
    *   Estimating Vπ by averaging sample returns from episodes
    *   First-visit Monte Carlo: averaging returns only for the first visit to a state in an episode.
    *   Every-visit Monte Carlo: averaging returns for every visit to a state in an episode.
*   Monte Carlo Control (Policy Optimization)
    *   Using Monte Carlo for policy improvement
    *   Exploring Starts: Every state-action pair is visited with non-zero probability.
    *   ε-Greedy Exploration: Selecting the greedy action with probability 1-ε, and a random action with probability ε.
*   On-Policy vs. Off-Policy Learning
    *   On-policy: Learning about the policy used to generate data.
    *   Off-policy: Learning about a different policy than the one used to generate data.
*   Importance Sampling
    *   Technique for estimating expected values under one distribution using samples from another distribution.
    *   Used in off-policy Monte Carlo methods.
    *   Weighted Importance Sampling vs. Ordinary Importance Sampling

**V. Temporal Difference (TD) Learning**

*   TD Prediction (Policy Evaluation)
    *   Estimating Vπ by bootstrapping: updating estimates based on other estimates.
    *   TD(0): Updating V(s) using the immediate reward and the estimated value of the next state: `V(s) ← V(s) + α [R + γ V(s') - V(s)]`
*   TD Control (Policy Optimization)
    *   SARSA (On-policy TD control): Updating Q(s, a) based on the current state, action, reward, next state, and next action: `Q(s, a) ← Q(s, a) + α [R + γ Q(s', a') - Q(s, a)]`
    *   Q-learning (Off-policy TD control): Updating Q(s, a) based on the current state, action, reward, next state, and the best action in the next state: `Q(s, a) ← Q(s, a) + α [R + γ maxa' Q(s', a') - Q(s, a)]`
*   Expected SARSA
    *   An on-policy TD control method that averages over possible actions in the next state: `Q(s, a) ← Q(s, a) + α [R + γ Σa' π(a'|s') Q(s', a') - Q(s, a)]`
*   Advantages and Disadvantages of TD Learning vs. Monte Carlo
    *   TD learns online, Monte Carlo learns after an episode.
    *   TD exploits the Markov property, Monte Carlo doesn't.
    *   TD is more sensitive to initial values.

**VI. Eligibility Traces**

*   λ-Return
    *   Generalizing Monte Carlo and TD(0)
    *   Averaging n-step returns with different weights.
*   TD(λ)
    *   Updating value functions using eligibility traces.
    *   Eligibility traces: A temporary record of state visits or action selections.
    *   Replacing Traces vs. Accumulating Traces
*   SARSA(λ)
    *   Combining SARSA with eligibility traces.
    *   Updating Q-values based on the TD(λ) error and eligibility traces.
*   Backward View of TD(λ)
    *   Understanding TD(λ) as propagating rewards backward through the episode.

**VII. Function Approximation**

*   Value Function Approximation
    *   Using parameterized functions to estimate value functions.
    *   Linear function approximation: `V(s, w) = wT x(s)`
    *   Non-linear function approximation: Neural Networks, Decision Trees, etc.
*   Gradient Descent Methods
    *   Stochastic Gradient Descent (SGD) for updating parameters.
    *   RMSprop, Adam, and other optimization algorithms.
*   Tile Coding
    *   A form of coarse coding for representing state spaces.
    *   Creating overlapping tilings of the state space.
*   Deep Reinforcement Learning
    *   Using deep neural networks as function approximators in RL.
    *   Deep Q-Networks (DQN)
        *   Experience Replay: Storing transitions in a replay buffer.
        *   Target Network: Using a separate network to compute target Q-values.
    *   Policy Gradient Methods
        *   REINFORCE: Updating the policy parameters based on the return from an episode.
        *   Actor-Critic Methods: Combining policy gradient and value-based methods.
        *   Advantage Actor-Critic (A2C)
        *   Asynchronous Advantage Actor-Critic (A3C)
        *   Proximal Policy Optimization (PPO)
        *   Trust Region Policy Optimization (TRPO)

**VIII. Policy Gradient Methods**

*   Policy Parameterization
    *   Representing policies using parameterized functions.
    *   Softmax policy: `π(a|s, θ) = exp(h(s, a, θ)) / Σb exp(h(s, b, θ))`
    *   Gaussian policy: `π(a|s, θ) = N(μ(s, θ), σ2)`
*   REINFORCE Algorithm
    *   Monte Carlo policy gradient algorithm.
    *   Updating policy parameters based on the return from an episode.
    *   `θ ← θ + α ∇θ log π(a|s, θ) Gt`
*   Actor-Critic Methods
    *   Combining policy gradient and value-based methods.
    *   Using an actor to learn the policy and a critic to estimate the value function.
    *   Advantage Actor-Critic (A2C): Using the advantage function to reduce variance.
*   Advanced Policy Gradient Methods
    *   Proximal Policy Optimization (PPO): Constraining policy updates to be close to the previous policy.
    *   Trust Region Policy Optimization (TRPO): Using a trust region to ensure stable policy updates.

**IX. Exploration vs. Exploitation**

*   ε-Greedy Exploration
    *   Selecting the greedy action with probability 1-ε, and a random action with probability ε.
*   Boltzmann Exploration (Softmax Action Selection)
    *   Selecting actions based on their estimated values.
    *   `P(a) = exp(Q(s, a) / τ) / Σa' exp(Q(s, a') / τ)`
*   Upper Confidence Bound (UCB)
    *   Balancing exploration and exploitation by selecting actions with high upper confidence bounds.
*   Thompson Sampling
    *   Maintaining a probability distribution over the unknown parameters of the environment.
    *   Sampling an action from the distribution and taking that action.
*   Intrinsic Motivation
    *   Rewarding the agent for exploring novel states or actions.
    *   Curiosity-driven exploration

**X. Multi-Agent Reinforcement Learning (MARL)**

*   Challenges in MARL
    *   Non-stationarity: The environment changes as other agents learn.
    *   Partial observability: Agents may not have complete information about the environment.
    *   Credit assignment: Determining which agent is responsible for a particular outcome.
*   Centralized Training with Decentralized Execution (CTDE)
    *   Training agents using a centralized critic, but executing policies in a decentralized manner.
    *   Counterfactual multi-agent policy gradients (COMA)
    *   Multi-agent deep deterministic policy gradient (MADDPG)
*   Self-Play
    *   Training agents by playing against themselves.
    *   Used in AlphaGo and other game-playing systems.
*   Communication
    *   Enabling agents to communicate with each other to improve coordination.
    *   Learning to communicate (CommNet, DIAL).

**XI. Advanced Topics and Research Directions**

*   Hierarchical Reinforcement Learning (HRL)
    *   Learning hierarchical policies to solve complex tasks.
    *   Options framework, Feudal RL.
*   Inverse Reinforcement Learning (IRL)
    *   Learning a reward function from expert demonstrations.
    *   Apprenticeship learning.
*   Imitation Learning
    *   Learning a policy directly from expert demonstrations.
    *   Behavior cloning, Dagger.
*   Safe Reinforcement Learning
    *   Learning policies that satisfy safety constraints.
    *   Constrained MDPs, Lyapunov-based safety.
*   Transfer Learning in RL
    *   Transferring knowledge learned in one environment to another.
*   Meta-Reinforcement Learning
    *   Learning how to learn RL algorithms.
*   Current research trends in RL (e.g., offline RL, representation learning).
