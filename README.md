# 🐦 Flappy Bird AI using Deep Q-Network (DQN)

## 📌 Overview

This project trains an AI agent to play Flappy Bird using **Deep Reinforcement Learning (DQN)**.
The agent learns optimal actions (flap or no flap) by interacting with the environment and maximizing rewards over time.

---

## 🎮 Environment

* Game: Flappy Bird (`FlappyBird-v0`)
* State Space: Bird position, velocity, pipe distance, etc.
* Action Space:

  * `0` → No Flap
  * `1` → Flap

---

## ⚙️ Tech Stack

* Python
* PyTorch
* Gymnasium
* flappy-bird-gymnasium
* NumPy
* PyGame

---

## 🔄 Workflow

### 1. Environment Setup

* Created using Gymnasium
* Real-time rendering using PyGame

---

### 2. Neural Network (DQN)

* Input: State features
* Hidden Layer: 256 neurons (ReLU)
* Output: Q-values for actions

---

### 3. Experience Replay

* Stores past experiences (state, action, reward, next state)
* Uses random sampling to stabilize learning

---

### 4. Epsilon-Greedy Strategy

* Starts with exploration (random actions)
* Gradually shifts to exploitation (model-based actions)

---

### 5. Training Loop

* Take action
* Observe reward
* Store experience
* Sample mini-batch
* Update model
* Sync target network

---

## ⚙️ Hyperparameters

* `epsilon_init`: 1
* `epsilon_min`: 0.05
* `epsilon_decay`: 0.9995
* `gamma`: 0.99
* `alpha (learning rate)`: 0.001
* `replay_memory_size`: 100000
* `mini_batch_size`: 32
* `network_sync_rate`: 10
* `reward_threshold`: 1000

---

## 🤖 Model Used

* Deep Q-Network (DQN)

---

## 📈 Results

* Agent learns to survive longer over episodes
* Rewards increase gradually with training
* Best model saved automatically

---

## 🏆 Key Features

* Experience Replay Buffer
* Target Network for stability
* GPU / CPU support
* Model saving & logging
* Configurable hyperparameters

---

## 📊 Key Insights

* Exploration is crucial in early training
* Epsilon decay helps balance learning
* Replay memory improves stability
* Target network prevents divergence

---

## ▶️ How to Run

```bash
git clone <repo-link>
cd flappy-dqn
pip install -r requirements.txt
python main.py flappybirdv0 --train
```

### ▶️ Test the Model

```bash
python main.py flappybirdv0
```

---

## 📌 Future Improvements

* Double DQN
* Dueling DQN
* Prioritized Experience Replay
* Hyperparameter tuning
* Deploy as interactive web demo

---

## 👤 Author

**Gurbachan Singh**
B.E. CSE | Chandigarh University
