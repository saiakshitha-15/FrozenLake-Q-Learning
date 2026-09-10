# 🧊 FrozenLake Q-Learning

A beginner-friendly Reinforcement Learning project using **Q-Learning** and the **Gymnasium FrozenLake-v1 environment**.

The agent learns through trial and error to navigate across a frozen lake, avoid holes, and reach the goal.

---

## 🎯 Project Objective

The main objective is to train an agent using **Q-Learning** so that it can:

- 🧊 Navigate across the frozen lake
- 🕳️ Avoid falling into holes
- 🏁 Reach the goal
- 🧠 Learn better actions through trial and error

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

Map Symbols
Symbol	Meaning
S	Starting point
F	Frozen surface
H	Hole
G	Goal

The agent can move Left, Down, Right, or Up and receives a reward of +1 for reaching the goal.
---

## 🧠 Q-Learning

The agent maintains a Q-table that stores the expected value of taking different actions from each state.

The learning process can be summarized as:

Observe State
      ↓
Choose Action
      ↓
Receive Reward
      ↓
Move to Next State
      ↓
Update Q-Table
      ↓
Repeat

An Epsilon-Greedy strategy is used to balance:

Exploration → Trying new actions
Exploitation → Choosing actions that have already been learned

##🌪️ is_slippery=True vs False

FrozenLake provides two different movement behaviors using the is_slippery parameter.

is_slippery=True
is_slippery=True

The environment is stochastic, meaning movement is unpredictable.

The agent may not always move in the direction it selected. This makes the environment more challenging.

Because of the randomness, even a trained agent may sometimes fall into a hole.

is_slippery=False
is_slippery=False

The environment becomes deterministic.

The agent moves exactly in the direction it selects, making the environment easier to understand and demonstrate.

## Comparison
Setting	Movement	Behavior
True	Unpredictable	More challenging
False	Predictable	Easier to demonstrate

Note: The same is_slippery setting should be used during both training and evaluation so that the Q-table matches the environment being used.

##🎥 Agent Visualization

After training, the learned Q-table is used to control the agent.

The agent's movements are rendered using Gymnasium and saved as a GIF.

##📂 Project Structure
FrozenLake-Q-Learning/
│
├── FrozenLake_Q_Learning.ipynb
├── frozenlake.gif
├── README.md
└── requirements.txt
##🔑 Key Concepts
Reinforcement Learning
Q-Learning
Q-Tables
Epsilon-Greedy Strategy
Exploration vs Exploitation
Stochastic vs Deterministic Environments
Gymnasium Environment Rendering
##🚀 Getting Started
Install the dependencies
pip install -r requirements.txt
Run the project

Open the following notebook in Jupyter Notebook or VS Code:

FrozenLake_Q_Learning.ipynb

Run the cells in order to train the agent and generate the visualization.

##🔗 Reference

Gymnasium – FrozenLake Documentation