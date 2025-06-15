# N-Queens 

## Overview
This Java application solves the N-Queens problem, where the goal is to place N queens on an N×N chessboard such that no two queens threaten each other. It uses a backtracking algorithm and provides a graphical interface built with Swing to visualize the solution process. Users can specify the board size, start the solver, and stop it as needed.

## Features
- **Backtracking Solver**: Implements a recursive backtracking algorithm to find a valid configuration for queen placements.
- **Graphical Visualization**: Displays the chessboard with alternating black/white cells and blue queens using a Swing JPanel.
- **User Interaction**: Allows users to input board size, start the solver, and stop it via GUI buttons.
- **Dynamic Board**: Supports variable board sizes entered at runtime.
- **Visualization Delay**: Includes a 500ms delay between steps for clear observation of the solving process.

## Requirements
- Java Development Kit (JDK) 8 

Uses standard Java libraries (`javax.swing`, `java.awt`), requiring no external dependencies.

## Project Structure
- `NQueensSolver.java`: Implements the backtracking algorithm and solver logic as a `Runnable` thread.
- `NQueensSolverGUI.java`: Defines the Swing-based GUI, including buttons and chessboard integration.
- `chessboard.java`: Custom `JPanel` for rendering the chessboard and queen positions.
- `README.md`: This documentation file.

## Example
To solve an 8-Queens problem:
- Run the program and enter `8` in the input dialog.
- Click "Start" to watch queens being placed on the 8×8 board.
- The solver places queens (blue ovals) on a black-and-white chessboard, ensuring no conflicts.

## Algorithm Details
- **Backtracking**: Places queens row by row, checking for safety (no conflicts in columns or diagonals). If a placement fails, it backtracks to try alternative positions.
- **Safety Check**: Verifies that a queen can be placed without conflicts in the same column or diagonals.
- **Threading**: Runs the solver in a separate thread to keep the GUI responsive, with interrupt support for stopping.
