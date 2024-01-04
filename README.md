# sudoku_stochastic_python
This repository contains a Python script for solving Sudoku puzzles using a stochastic approach, which includes elements of randomness and probability.

## Description

The script uses a combination of techniques to fill in a Sudoku grid and iteratively improve the solution towards a valid Sudoku configuration. The key features of the script include:

- **Grid Initialization**: The script starts with a predefined Sudoku puzzle, represented as a string and then converted into a NumPy array for easier manipulation.
- **Random Block Filling**: Initially fills the 3x3 blocks of the Sudoku grid randomly with numbers not already present in the block.
- **Cost Function**: Calculates the number of errors (incorrectly filled rows or columns) in the grid.
- **Stochastic Approach**: Iteratively flips the numbers within the blocks and evaluates if the change leads to a reduction in the number of errors, using a probability-based approach.

## Methodology
- **Cost Calculation**: The script calculates the cost as the total number of errors (duplicates in rows and columns) in the current state of the Sudoku grid.
- **Proposed State Generation**: Randomly selects two numbers within a block and swaps them to create a new proposed state.
- **State Evaluation**: Compares the cost (number of errors) of the new state with the current state. If the new state has a lower cost, it is more likely to be accepted as the new current state.
- **Convergence**: The process continues iteratively, with the system gradually cooling down (reducing the probability of accepting worse states), until a solution is found or a certain number of iterations are reached.

## Limitations and Scope
- The stochastic nature means that the script may not always find a solution, and the solution time can vary.
- The script currently works with a predefined puzzle but can be modified to accept user input.

## Future Enhancements
- Enhance the algorithm to improve the solution speed and reliability.
- Implement a user interface for puzzle input and visualization.
- Explore other optimization techniques for Sudoku solving.
