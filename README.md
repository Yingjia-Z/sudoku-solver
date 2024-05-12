## Sudoku Solver

This project uses 3 distinct CSP-based methods to solve Sudoku puzzles efficiently. Each approach incorporates different strategies and heuristics to speed up solving times.

### Overview
In the [`solver`](sudoku.ipynb) Jupyter notebook:

#### Part A: CSP Formalization
- **Formal Description**: Provides a formal CSP description of Sudoku, detailing variables, their domains, and the constraints among them.

#### Part B: Solver Implementations
- **Version A**: Standard backtracking search (no forward checking, random variable order, random value order).
- **Version B**: Standard backtracking search + forward checking (random variable order, random value order).
- **Version C**: Standard backtracking search + forward checking + three heuristics to order variables and values, using random selection to break ties.
  - Three heuristics:
    - Most Constrained Variable
    - Most Constraining Variable
    - Least-Constraining Value

#### Part C: Performance Evaluation
- **Testing**: Runs each version on test puzzles of varying difficulty levels (easy, medium, difficult, and evil) to compare performance.
- **Metrics Reported**:
  - **Time Performance**: Reports average time and standard deviation to complete each puzzle over 50 trials.
  - **Efficiency**: Details the average number of nodes expanded and the standard deviation for each puzzle. Nodes are considered expanded when they are removed from the queue and their children are added.

#### Notes
- **Run Feasibility**: For Versions A and B, consider reducing the number of trials from 50 to a more feasible number due to time constraints.
- **High Efficiency**: Version C solves puzzles of all difficulty levels in under 0.136 seconds.
