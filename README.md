# Reinforcement Learning




- [Reinforcement Learning](#reinforcement-learning)
  - [Multi-Armed Bandit](#multi-armed-bandit)
    - [Policies](#policies)
      - [Epsilon-Greedy](#epsilon-greedy)
      - [Optimistic Initial Value](#optimistic-initial-value)
      - [Upper Confidence Bound (UCB)](#upper-confidence-bound-ucb)
      - [Softmax](#softmax)
      - [Bayesian](#bayesian)
  - [Model-Based RL](#model-based-rl)
    - [Markov Decision Process (MDP)](#markov-decision-process-mdp)
      - [Bellman Equation](#bellman-equation)
      - [Policy Iteration](#policy-iteration)
      - [Value Iteration](#value-iteration)
    - [Dynamic Programming \& Bellman Optimality](#dynamic-programming--bellman-optimality)
    - [Non-Linear Dynamics](#non-linear-dynamics)
      - [Optimal Control and HJB](#optimal-control-and-hjb)
  - [Model Free RL](#model-free-rl)
    - [Gradient Free](#gradient-free)
      - [Off Policy](#off-policy)
        - [Q-Learning](#q-learning)
      - [On Policy](#on-policy)
        - [SARSA](#sarsa)
    - [Gradient-Based](#gradient-based)
      - [Policy Gradient Optimization](#policy-gradient-optimization)
  - [Deep RL](#deep-rl)
    - [Actor Critic](#actor-critic)
    - [Deep MPC](#deep-mpc)
    - [DQN](#dqn)
    - [Deep Policy Network](#deep-policy-network)


## Multi-Armed Bandit

### Policies
#### Epsilon-Greedy
Usually $Q(S) = 0$ is used as initial value
\
$\pi=\left\{
\begin{matrix}
\epsilon-greedy & prob= 1-p \\ 
random & prob= p 
\end{matrix}
\right.$

#### Optimistic Initial Value

Basically, this is the same epsilon-greedy policy with initial $Q(S) \neq 0$
\
$
\pi=\left\{
\begin{matrix}
\epsilon-greedy & prob= 1-p \\ 
random & prob= p 
\end{matrix}
\right.$



#### Upper Confidence Bound (UCB)
#### Softmax

A softmax policy isn't a specific policy itself, but rather **a way to convert estimated state values into action probabilities**. It's commonly used with other policy approaches, particularly those that estimate state values (e.g., value iteration, Q-learning).

**How it works?**

- **State Value Estimation**: The reinforcement learning algorithm estimates the expected future reward (or Q-value) for each possible action in a given state.
- **Softmax Function**: These estimated values are then fed into a softmax function. The softmax function takes a vector of real numbers and transforms them into a probability distribution between 0 and 1. The key characteristic of the softmax function is that it amplifies the differences between the values.
- **Action Probabilities**: The output of the softmax function becomes a set of probabilities for each action. Actions with higher estimated values will have a higher probability of being chosen, while those with lower values will have a lower probability.

**Benefits of Softmax Policy**

- **Exploration-Exploitation Trade-off**: Softmax provides a smooth trade-off between exploration and exploitation. It allows the agent to try different actions (explore) while still favoring actions with higher estimated rewards (exploit). This is particularly beneficial compared to a greedy approach (always choosing the highest value action) which can get stuck in local optima.
- **Gradient-based Optimization**: The output probabilities from the softmax function can be easily integrated with gradient-based optimization algorithms commonly used in reinforcement learning. This allows the policy to be updated efficiently based on the rewards received.

**Drawbacks of Softmax Policy**

- **High Variance**: If the estimated state values have high variance (uncertainty), the softmax probabilities can also be highly variable, leading to potentially suboptimal exploration. Techniques like experience replay can help reduce this variance.
- **Computational Cost**: While relatively cheap, calculating the softmax function for every action in a state can become computationally expensive for environments with a large number of actions.
#### Bayesian

## Model-Based RL

### Markov Decision Process (MDP)

#### Bellman Equation

$V^{\pi}(S)=\sum_{S'} P(S'|S,\pi(S))[R(S,\pi(S),S')+\gamma V^{\pi}(S')]$

#### Policy Iteration

#### Value Iteration

### Dynamic Programming & Bellman Optimality

### Non-Linear Dynamics
#### Optimal Control and HJB

## Model Free RL

### Gradient Free

#### Off Policy
##### Q-Learning

#### On Policy
##### SARSA

### Gradient-Based
#### Policy Gradient Optimization

## Deep RL
### Actor Critic
### Deep MPC
### DQN
### Deep Policy Network
