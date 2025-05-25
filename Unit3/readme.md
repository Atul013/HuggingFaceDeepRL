# 📘 Reinforcement Learning Unit 3 Glossary  
## Deep Q-Learning Foundations

In this unit, we explore how to scale Q-Learning to complex environments using deep learning. This section introduces key concepts such as tabular methods, Deep Q-Networks (DQN), and strategies to stabilize training.

---

## 📊 Tabular Method

- A method used when the **state and action spaces are small enough** to be represented in tables or arrays.
- **Q-Learning** is an example of a tabular method where a table stores the value for each state-action pair.
- Works well only for small, discrete environments due to memory and scalability constraints.

---

## 🧠 Deep Q-Learning (DQN)

- Uses a **neural network** to approximate Q-values for each action given a state.
- Solves problems with **large observational spaces** (e.g., images) where tabular approaches become impractical.
- Network outputs a vector of Q-values — one per action — allowing the agent to choose the best action.

---

## ⏳ Temporal Limitation

- Occurs when the environment uses **frames** (like pixels from a game) to represent the state.
- A single frame often lacks **temporal information**, making it hard for the agent to understand motion or changes over time.
- Solved by **stacking multiple frames together**, giving the agent context about movement and dynamics.

---

## 🔁 Phases of Deep Q-Learning

| Phase     | Description |
|-----------|-------------|
| **Sampling** | The agent performs actions and stores experience tuples `(state, action, reward, next_state, done)` in a replay memory. |
| **Training** | Random batches of experiences are sampled from the memory, and the neural network updates its weights using gradient descent. |

---

## 🛡️ Solutions to Stabilize Deep Q-Learning

### 🧠 Experience Replay

- Stores past experiences in a **replay buffer**.
- During training, **random mini-batches** are sampled from this buffer.
- Helps reduce correlation between consecutive observations.
- Prevents oscillation and divergence in Q-value estimation.
- Allows the agent to learn from past experiences multiple times.

### 🎯 Fixed Q-Target

- In DQN, both the **Q-value** and the **Q-target** are computed using the same network, causing instability.
- To fix this, a **separate target network** is used to compute the Q-target.
- The target network is updated less frequently (every C steps) by copying weights from the main DQN.
- This stabilizes learning and prevents the target from shifting too quickly.

### 🔁 Double DQN

- Addresses the problem of **overestimation of Q-values** in standard DQN.
- Uses **two networks**:
  - **DQN Network**: Selects the best action for the next state.
  - **Target Network**: Computes the Q-value of that selected action.
- Decouples **action selection** from **target calculation**, reducing bias.
- Leads to more stable and faster convergence during training.

---

## ✅ Summary Table: Stabilization Techniques

| Technique            | Purpose                                                                 | How It Works |
|----------------------|-------------------------------------------------------------------------|--------------|
| Experience Replay    | Breaks correlation in data and improves sample efficiency                 | Stores and randomly samples past experiences |
| Fixed Q-Target       | Stabilizes Q-target computation                                         | Uses separate slowly-updated network |
| Double DQN           | Reduces overestimation of Q-values                                      | Uses two networks: one for action, one for target |
