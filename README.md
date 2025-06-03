# Optimization Techniques Feb-Jun 2025

## Overview
This repository contains implementations of metaheuristic algorithms covered in class between February and June 2025. All code focuses on solving combinatorial optimization problems, with a special emphasis on the 0/1 Knapsack Problem.

## GRASP + ILS Implementation
The `grasp_ils/` folder includes a **reactive GRASP + ILS** approach for solving the 0/1 Knapsack Problem. In this implementation:
- **GRASP** (Greedy Randomized Adaptive Search Procedure) constructs an initial solution by iteratively building a restricted candidate list based on benefit-to-weight ratio.
- **ILS** (Iterated Local Search) perturbs the current solution and then applies a local-improvement routine to escape local optima.
- The **reactive** component dynamically updates the GRASP’s α-parameter (which controls the greediness/randomness balance) based on run-time performance metrics.

## Usage
1. Navigate to the `grasp_ils/` directory.
2. Ensure all dependencies (e.g., Python 3.x) are installed.
3. Run:
   ```bash
   python main_knapsack.py <input_file>

n W
d₁ w₁
d₂ w₂
…
dₙ wₙ

optimization-techniques/
├── grasp_ils/
│   ├── main_knapsack.py
│   ├── grasp.py
│   ├── ils.py
│   ├── utils.py
│   └── README.md  ← this file (explains how to run GRASP+ILS)
├── other_metaheuristics/
│   ├── tabu_search.py
│   ├── simulated_annealing.py
│   └── ...
└── README.md       ← you are here

@book{talbi2009metaheuristics,
  title     = {Metaheuristics: From Design to Implementation},
  author    = {Talbi, E.\,G.},
  isbn      = {9780470496909},
  lccn      = {2009017331},
  series    = {Wiley Series on Parallel and Distributed Computing},
  url       = {https://books.google.com.mx/books?id=SIsa6zi5XV8C},
  year      = {2009},
  publisher = {Wiley}
}

