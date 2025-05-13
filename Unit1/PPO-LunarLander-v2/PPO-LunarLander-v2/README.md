# PPO-LunarLander-v2

This repository contains the implementation of Proximal Policy Optimization (PPO) applied to the OpenAI Gym environment `LunarLander-v2`. The goal is to train an agent to land a spacecraft on the moon safely using reinforcement learning techniques.

### Overview

The `LunarLander-v2` environment is a classic reinforcement learning problem where an agent must control a spacecraft to land safely on the lunar surface. The agent receives observations such as the position, velocity, and angle of the spacecraft, and must output actions like thrust and orientation adjustments.

This repository uses the Proximal Policy Optimization (PPO) algorithm to train the agent. PPO is a state-of-the-art policy gradient method that balances exploration and exploitation effectively.

### Video Preview

Here is a preview of the trained agent landing successfully:

[![Agent Landing Successfully](replay.mp4)](replay.mp4)

### Model Details

### Algorithm
- **Algorithm**: Proximal Policy Optimization (PPO)
- **Environment**: OpenAI Gym `LunarLander-v2`
- **Observation Space**: Continuous (position, velocity, angle, etc.)
- **Action Space**: Discrete (thrust and orientation adjustments)

### Hyperparameters
- **Learning Rate**: 0.0003
- **Batch Size**: 64
- **Number of Epochs**: 10
- **Clip Range**: 0.2
- **Discount Factor (γ)**: 0.99
- **GAE Lambda**: 0.95

### Training Process
- The agent was trained over multiple episodes.
- The training process used a replay buffer to store experiences and update the policy network periodically.
- The policy network is a feedforward neural network with two hidden layers, each containing 64 neurons and ReLU activations.

### Files in the Repository

- **`ppo-LunarLander-v2/`**: Contains the source code for the PPO implementation.
- **`config.json`**: Configuration file for the experiment, including hyperparameters.
- **`ppo-LunarLander-v2.zip`**: Zipped version of the trained model files.
- **`replay.mp4`**: Video showcasing the agent's performance after training.
- **`results.json`**: JSON file containing training metrics and results.

### Model Index & Metadata

The following metadata describes the model and its performance:

```yaml
library_name: stable-baselines3
tags:
  - LunarLander-v2
  - deep-reinforcement-learning
  - reinforcement-learning
  - stable-baselines3
model-index:
  - name: PPO
    results:
      - task:
          type: reinforcement-learning
          name: reinforcement-learning
        dataset:
          name: LunarLander-v2
          type: LunarLander-v2
        metrics:
          - type: mean_reward
            value: 245.67 +/- 68.28
            name: mean_reward
            verified: false
```
### Ways to Contribute: 

    Improve the training hyperparameters.
    Add more visualization tools.
    Extend the implementation to other environments.
    Fix bugs or improve documentation.
     
