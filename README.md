# **Markov Decision Process (MDP) - Grid World Simulation**
This repository contains an implementation of the Markov Decision Process (MDP) in a 3x3 grid environment. The agent navigates the grid to reach a goal while maximizing rewards, demonstrating core MDP principles such as states, actions, rewards, and transition probabilities.

## **Overview**
A Markov Decision Process (MDP) is a mathematical framework for decision-making under uncertainty, commonly used in reinforcement learning, robotics, and AI planning. It is defined by the tuple **(S, A, P, R, γ)**:
- **S (States):** Possible positions of the agent in the grid.
- **A (Actions):** Possible moves (Up, Down, Left, Right).
- **P (Transition Probability):** Probability of transitioning to a new state.
- **R (Reward):** Immediate reward received for an action.
- **γ (Discount Factor):** Future reward discounting.

## **Problem Statement**
Simulate an agent navigating a **3x3 grid** where:
- The agent starts at **(0,0)** (top-left).
- The goal is at **(2,2)** (bottom-right).
- Each move has a reward of **-1**.
- Reaching the goal gives a reward of **+10**.
- The agent aims to **maximize cumulative rewards**.

## **Concepts Used**
- **Markov Decision Process (MDP)**
- **Bellman Equation for Optimal Policy**
- **Grid World Representation**
- **Path Visualization using Heatmap**

## **Implementation Details**
### **1. Grid Environment**
A **3x3 grid** where the agent starts at (0,0) and aims to reach (2,2).

### **2. Actions**
The agent can move in **four directions**:
- **UP** (-1, 0)
- **DOWN** (+1, 0)
- **LEFT** (0, -1)
- **RIGHT** (0, +1)

### **3. Rewards**
- **-1** for each step.
- **+10** for reaching the goal.

### **4. Transition Probability**
- **Deterministic (1.0):** The agent always moves as intended unless at the grid boundary.

## **Procedure**
1. Define the **3x3 grid** environment.
2. Assign **states**, **actions**, and **rewards**.
3. Implement **MDP transition rules**.
4. Simulate agent movement with random action selection.
5. Track **total rewards** and **path taken**.
6. **Visualize** agent’s path using a **heatmap**.

## **Code Implementation**
### **Key Functions**
- `get_next_state()`: Determines the next state based on the chosen action.
- `run_mdp()`: Simulates agent movement, tracks rewards and path.
- `visualize_path()`: Generates a heatmap of the agent's path.

### **Execution**
Run the script to simulate agent navigation and visualize results:
```python
if __name__ == "__main__":
    path_taken = run_mdp()
    visualize_path(path_taken)
```

## **Visualization**
- A **heatmap** displays the agent's path.
- **Color intensity** represents visit count.
- The **goal state is highlighted**.

## **Results & Observations**
- The **agent navigates randomly**, with steps and rewards logged.
- **Path visualization** provides insights into movement dynamics.
- This **grid-world MDP** lays the foundation for real-world applications in **robotics, AI, and reinforcement learning**.

## **Conclusion**
This project effectively demonstrates **MDP fundamentals** in a simple environment. It highlights:
- **Decision-making under uncertainty.**
- **Reinforcement learning concepts.**
- **Path visualization for interpretability.**

This example serves as a stepping stone for **advanced MDP applications** in AI-driven decision-making and policy optimization.

---

### **Future Enhancements**
- Implement **policy iteration** and **value iteration** for optimal decision-making.
- Introduce **stochastic transitions** for real-world applicability.
- Extend to **larger grid environments** with complex constraints.

---
