# Ghosts In The Maze
Implementing and analyzing various search algorithms to navigate a dynamically changing maze environment filled with moving ghosts.
Overview

This project, completed as part of the Computer Science course at Rutgers University (Fall 2022), focuses on implementing and comparing various search algorithms to solve the problem of navigating a maze infested with ghosts. The goal is to create agents that can find paths through the maze while avoiding moving ghosts, which introduce dynamic and unpredictable elements to the environment.
Project Structure
1. Environment

The environment is a randomly generated maze represented as a 51x51 grid. Each cell in the grid can either be open (unblocked) or obstructed (blocked). The generation process ensures that there is always a path from the start (upper left corner) to the goal (lower right corner).
2. Agent

The agent starts in the upper left corner of the maze and aims to reach the lower right corner. It can move up, down, left, or right, but only through unblocked cells. The agent must avoid ghosts, which move randomly within the maze.
3. Ghosts

Ghosts start at random locations in the maze that are reachable from the start. They can move into adjacent unblocked cells or sometimes move into blocked cells based on certain probabilities. If a ghost occupies the same cell as the agent at any time, the agent dies.
Agent Strategies

Four different strategies were implemented for the agent to navigate the maze:

    Agent 1: The Ignorant Planner
        Plans the shortest path through the maze and executes it without considering the ghosts.
        Efficient in terms of planning but highly vulnerable to dynamic obstacles (ghosts).

    Agent 2: The Reactive Planner
        Re-plans its path at each timestep based on the current positions of the ghosts.
        More adaptive to changes but computationally expensive due to continuous re-planning.

    Agent 3: The Forecasting Planner
        Simulates future movements of ghosts to choose the safest path.
        Balances between planning and forecasting but may still face challenges if all paths are blocked.

    Agent 4: The Custom Strategy
        A custom strategy developed to outperform the previous agents.
        Balances efficiency and adaptability, potentially considering ghost proximity and alternative paths.

Analysis

The performance of each agent strategy was analyzed by running experiments with varying numbers of ghosts. Key points of analysis include:

    Success rates of each agent in reaching the goal without dying.
    Computational efficiency and bottlenecks encountered during implementation.
    Comparison of agents' performance under different conditions (e.g., total awareness vs. limited visibility of ghosts).

Graphs and data from these experiments provide insights into which strategies are most effective under different scenarios.
Usage

To run the project, open the provided Jupyter Notebook (Ghosts_in_the_Maze.ipynb) in an appropriate environment (e.g., Jupyter Lab, Google Colab). The notebook contains detailed comments and explanations to guide you through the implementation and experimentation process.
Requirements

    Python 3.x
    Jupyter Notebook
    Required libraries: numpy, matplotlib, random
