# Reinforcement Learning: REINFORCE & Deep Q‑Learning on CartPole and LunarLander

This repository contains the implementation for a class assignment in an Autonomous Agents / Deep Reinforcement Learning course. The project is divided into two main parts:
1. **Policy‑gradient methods on CartPole using REINFORCE**, with and without baselines.
2. **Value‑based methods using Deep Q‑Learning** on CartPole and LunarLander.

The goal of the assignment is to compare policy‑gradient variants, understand the effect of baselines on variance reduction, and successfully solve classic control environments using Deep Q‑Learning.

---

## 🎯 Project Overview
### Part 1 — REINFORCE Variants on CartPole
In the first section of the assignment, the CartPole‑v1 environment is solved using three versions of the REINFORCE algorithm:

- **REINFORCE (no baseline)**: the simplest Monte‑Carlo policy‑gradient method using raw returns.
- **REINFORCE with Standardized Returns**: reduces variance by normalizing episode returns.
- **REINFORCE with a Value Baseline**: trains a value network as a learned baseline to compute the advantage.

The objective is to compare learning curves and observe how baselines affect stability, convergence speed, and variance.

---

### Part 2 — Deep Q‑Learning on CartPole and LunarLander
In the second part of the assignment, the focus moves to value‑based reinforcement learning using Deep Q‑Networks (DQN). Both environments use the standard DQN ingredients:

- Experience replay buffer
- Target network
- ε‑greedy exploration
- Neural network Q‑function approximation

The environments solved are:
- **CartPole‑v1**: a simple control task where DQN learns quickly.
- **LunarLander‑v2**: a much more challenging control problem that requires careful tuning to stabilize learning.

---

## 🧠 Methods
### REINFORCE Variants
- **Policy network**: maps states to action probabilities.
- **Monte Carlo estimation**: returns computed at episode end.
- **Baselines**: used to reduce gradient variance.
- **Comparison metric**: average episodic reward during training.

### Deep Q-Learning
- **Q‑Network**: predicts Q(s, a).
- **Experience Replay**: random minibatches break correlation.
- **Target Network Updates**: stabilize temporal difference learning.

![Demo GIF](CartPole_dqn.gif)
![Demo GIF](LunarLander_dqn.gif)