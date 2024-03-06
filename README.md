# Reinforcement Learning

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
#### Bayesian

## Model-Based RL

### Markov Decision Process (MDP)

#### Bellman Equation

$V^{\pi}(S)=\sum_{S'} P(S'|S,\pi(S))[R(S,\pi(S),S')+\gamma V^{\pi}(S')]$

#### Policy Iteration

#### Value Iteration

### Dynamic Programming & Bellman Optimality

#### Non-Linear Dynamics

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
