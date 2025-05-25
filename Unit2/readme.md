# 📘 Reinforcement Learning Unit 2 Glossary
### 🧠 Strategies to Find the Optimal Policy 

In reinforcement learning, the ultimate goal is to find an optimal policy  — a strategy that tells the agent what action to take in each state to maximize cumulative reward. 

There are two main categories of methods for finding such a policy: 
🛠️ Policy-Based Methods 

 - The policy is learned directly , often using a neural network .
 - Given a state, the neural network outputs the action the agent should take .
 - As the agent gains more experience from the environment, the policy (network) is updated to improve decision-making.
 - No value function is used — the policy is the model itself.
     

✅ Pros :   

 - Can be more direct and effective in high-dimensional or continuous action spaces.
     

❌ Cons :   

  - Often suffers from high variance.
  - May get stuck in local optima.
     

💹 Value-Based Methods 

   - Instead of learning a policy directly, we learn a value function : 
   - State-value function V(s) : Expected return starting from state s and following the policy.
   - Action-value function Q(s,a) : Expected return starting from state s, taking action a, then following the policy.
         

  - Based on this value function, we define a policy  (e.g., greedy or epsilon-greedy). 
     

### 🔍 Exploration vs. Exploitation Strategies 
🎯 Greedy Strategy 

  - Always chooses the action with the highest expected reward (exploitation only ).
  - Does not explore new actions.
  - Risk: May miss better long-term rewards due to lack of exploration.
     

🔄 Epsilon-Greedy Strategy 

  - Balances exploration  and exploitation .
  - With probability 1 - ε , choose the best-known action.
  - With probability ε , choose a random action.
  - Typically, ε decreases over time , shifting focus toward exploitation.
<br>

### 🚦 On-Policy vs Off-Policy Algorithms

| Type        | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| **On-policy**  | Uses the same policy for both acting and updating (e.g., SARSA).            |
| **Off-policy** | Learns from actions taken by a different policy than the one being improved (e.g., Q-Learning). |
<br>

### ⏱️ Learning Strategies: Monte Carlo vs Temporal Difference

| Method                  | Description                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Monte Carlo (MC)**    | Learns at the end of an episode by using the full return from a complete trajectory. <br> Requires episodic tasks.                        |
| **Temporal Difference (TD)** | Learns after every step using bootstrapping (estimating values based on other estimates). <br> Works for both episodic and continuous tasks. |
     
