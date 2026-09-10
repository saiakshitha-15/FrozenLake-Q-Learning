# 🧊 FrozenLake Q-Learning

A beginner-friendly Reinforcement Learning project using **Q-Learning** and the **Gymnasium FrozenLake-v1 environment**.

The agent learns through trial and error to navigate across a frozen lake, avoid holes, and reach the goal.

---

## 🎯 Project Objective

The main objective of this project is to train an agent using **Q-Learning** so that it can:

- 🧊 Move across the frozen lake
- 🕳️ Avoid falling into holes
- 🏁 Reach the goal
- 🧠 Learn the best actions through trial and error

---

## 🛠️ Technologies Used

- 🐍 Python
- 🎮 Gymnasium
- 🔢 NumPy
- 🎞️ ImageIO
- 🎨 Pygame
- 📓 Jupyter Notebook

---

## 🌊 FrozenLake Environment

This project uses the standard **4×4 FrozenLake-v1** environment.

```text
S F F F
F H F H
F F F H
H F F G
Symbol	Meaning
S	Starting point
F	Frozen surface
H	Hole
G	Goal

The agent can move Left, Down, Right, or Up and receives a reward of +1 for reaching the goal.

🧠 Q-Learning

The agent maintains a Q-table containing the expected value of taking each action from every state.

During training, it repeatedly:

Observe State → Choose Action → Receive Reward → Update Q-Table

An Epsilon-Greedy strategy is used to balance exploration of new actions with exploitation of learned actions.

🌪️ is_slippery=True vs False

FrozenLake provides two different movement behaviors.

is_slippery=True

The environment is stochastic. The agent may not always move in the direction it selected.

This makes the environment more challenging and unpredictable. Therefore, even a trained agent can sometimes fall into a hole.

is_slippery=False

The environment becomes deterministic. The agent moves exactly in the direction it selects.

This makes it easier to demonstrate a consistent learned path.

Setting	Movement	Behavior
True	Unpredictable	More challenging
False	Predictable	Easier to demonstrate

Note: The same is_slippery setting should be used during both training and evaluation so that the learned Q-table matches the environment.

🎥 Agent Visualization

The trained agent is rendered using Gymnasium and saved as a GIF.

🛠️ Tech Stack
Python
Gymnasium
NumPy
Jupyter Notebook
Pygame
ImageIO
📂 Project Structure
FrozenLake-Q-Learning/
│
├── FrozenLake_Q_Learning.ipynb
├── frozenlake.gif
├── README.md
└── requirements.txt

Key Concepts
Reinforcement Learning
Q-Learning
Q-Tables
Epsilon-Greedy Strategy
Exploration vs Exploitation
Stochastic vs Deterministic Environments
Gymnasium Environment Rendering

🔗 Reference

Gymnasium – FrozenLake Documentation