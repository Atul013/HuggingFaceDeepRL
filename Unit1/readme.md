

# 📘 Reinforcement Learning Unit 1 Glossary

> *This is a community-created glossary.*


## 🤖 Agent

An **agent** learns to make decisions by trial and error, receiving rewards or punishments from its surroundings based on its actions.

## 🌍 Environment

The **environment** is the simulated world where an agent interacts and learns. It defines the rules and dynamics within which the agent operates.

## 🔄 Markov Property

A process has the **Markov Property** if the next state depends only on the current state and action, not on the sequence of events that preceded it.

> *"The future is independent of the past given the present."*

## 👁️ Observations / State

- **State**: A complete description of the environment at a given time.
- **Observation**: A partial or noisy view of the state, often used when the full state isn't accessible.

## 🕹️ Actions

- **Discrete Actions**: Finite set of possible actions (e.g., left, right, up, down).
- **Continuous Actions**: Infinite range of possible actions (e.g., steering angle in autonomous driving).

## 💰 Rewards and Discounting

- **Rewards**: Feedback signal indicating how good or bad an action was.
- **Reward Hypothesis**: All goals in RL can be described as maximizing cumulative reward over time.
- **Discounting**: Future rewards are worth less than immediate ones. The discount factor γ ∈ [0, 1] controls this trade-off.

## 📜 Tasks

- **Episodic Task**: Has a clear start and end (e.g., completing a level in a game).
- **Continuous Task**: No explicit end; continues indefinitely (e.g., real-time control systems).

## 🔍 Exploration vs. Exploitation Trade-Off

- **Exploration**: Trying new actions to discover potentially better outcomes.
- **Exploitation**: Using known information to maximize current reward.
- **Trade-Off**: Balancing exploration and exploitation to ensure long-term success.

## 🧠 Policy

- **Policy**: Strategy used by the agent to decide actions based on the current state. Think of it as the "brain" of the agent.
- **Optimal Policy**: A policy that maximizes the expected cumulative reward over time.

### 🛠️ Policy-Based Methods

- Directly learn a policy.
- Map states to actions or probability distributions over actions.

### 💹 Value-Based Methods

- Learn a value function instead of a direct policy.
- Estimate the expected return (value) of being in a state (or taking an action in a state), guiding decision-making.
