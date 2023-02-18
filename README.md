# ChessAIJulia

A university project for programming an AI for Chess using Julia

## Contents

### /Julia

This directory contains all the Jupyter Notebooks written in Julia needed for the AI.

| Notebook                | Function                                                                          |
| ----------------------- | --------------------------------------------------------------------------------- |
| AlphaBetaPruning.ipynb  | **AI** that calculates a move using the Alpha-Beta-Pruning algorithm              |
| ChessJL Summary.ipynb   | A summary of the most important methods that Chess.jl provides                    |
| EvaluatePosition.ipynb  | Evaluation a chess position refers how strong the position or one move is         |
| Minimax.ipynb           | **AI** that calculates a move using the minimax algorithm                         |
| PGN_Export_.ipynb       | Export games as PGN files                                                         |
| PGN_Import_.ipynb       | Import PGN files as Games                                                         |
| Play.ipynb              | **Play** as a user against one of the chess                                       |
| Random Chess.ipynb      | **AI** that plays a random move out of a List of all possible moves using a seed  |
| ValidateUserInput.ipynb | Check is the user input in legal moves                                            |
| style.css               | Contains some css for using the whole width of a notebook                         |

The notebooks ending on `.._testing.ipynb` are tests for the corresponding notebook.

### /Games
This directory contains PGN (Portable Game Notation) files of chess games played against written AIs in the `Play.ipynb`. They will be saved to later on find errors to see how the chess AIs behaved.

### example_positions.txt
A text document containing chess positions in Forsyth–Edwards Notation (FEN) sorted by a meaning for testing. E.g. Positions with an obvious best move, Positions where black gets checkmated, etc.