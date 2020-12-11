
# 1 Introduction

## Course Topics 

- Part I: Intelligence from Computation
    - Fast search / planning
    - Constraint satisfaction
    - Adversarial and uncertain search
- Part II: Intelligence from Data 
    - Bayes' nets
    - Decision theory
    - Machine learning
- Throughout: Application
    - Natural language, vision, robotics, games, ...


# 2 Uninformed Search

1. DFS  depth first search
2. BFS  breadth first search
3. UCS  uniform cost search


# 3 Informed Search

- A\*
    - UCS + Greedy Search
    - heuristic
        - tree search: Admissible Heuristic
        - graph search: consistency Heuristic to solve the problem caused by `closed` set
    - often use relaxed-problem heuristic
    - semi-Lattice

# 4 CSP

- Backtracking Search
    - the basic **uninformed** algorithm for solving CSPs
    - DFS + variable-ordering + fail-on-violation
- Improved Backtracking
    - filtering 
        - forward checking + arc consistency
    - ordering : **hardest variable, easiest value**
        - Variable: MRV  minimum remaining values
        - Values: LCV  least constraining value
- Improving Structure 
- Iterative Improvement
    - randomly pick variable
    - reassign a value that violates the fewest constraints


# 5 Adversarial Search

- Minimax search
- Expectimax Search (Uncertainty)
- formalize the underlying uncertain-result problems as **Markov Decision Processes**


# MDP

- Solve MDP
    1. value iteration
    2. policy iteration
        - 
        ```python
        Repeat:
            Policy evaluation , start from old value, iterate until converge, maybe run 100 times
            Policy improvement, do it only once
        ```
- If we don't have the T or R , then it was not planning, it was learning!


# Reinforcement Learning

- RL 
    1. Model-based
        - learn probability distribution -> solve MDP
    2. Model-free
        - learn average values, not T & R
            1. directly learn from state value -> no correlations between stats
            2. learn from Q-values 
        - Big Idea: Temporal Difference Learning
- Approximated Q-Learning
    - learning weights

# Bayes Net

- Bayes’nets / graphical models help us express conditional independence assumptions
- Assumptions
    - P(xᵢ |x₁,...,x<sub>i-1</sub>) = P(xᵢ|parent(Xᵢ) )
- ![](https://github.com/mebusy/notes/raw/master/imgs/cs188_BNsR_probInBNs_product.png)
- D-separation
    - causal chains
    - common cause
    - common effect (V-shape)
- causal chain , and common cause can represent same distributiosn, they are effectively equivalent structures.


# Neural Network

http://playground.tensorflow.org/




