# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  

A: The naked twins problem occurs when we have exactly two boxes within the same unit with the same two values. We know that other boxes in their unit cannot contain these values. For example if box F1 and F2
both have the values 1 and 2 then this places a constraint on the rest of the units. That is, we can
remove values 1 and 2 from the rest of the unit since we know the values can only be located in F1 and F2. This is an example of constraint propagation where we use a constraint to help us eliminate choices and
reduce the overall search space. We were already using only choice and eliminate for constraint propagation but solving the naked twins problem further reduces the search space.


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  

A: The diagonal sudoku problem occurs when we have diagonal units running through the centre of the board
along with our regular board. In the same way that we applied constraint propagation within the naked twins problem, we can apply this within the diagonal sudoku problem to reduce the overall search space. We know that having diagonal units creates further constraints on board. We apply the same strategy that we do for a normal Sudoku when approaching this problem. We eliminate the units from peers that have a single solved box. We call only choice to find values where there is only a single choice for the unit. We apply the naked twins strategy as above.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project.
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py
