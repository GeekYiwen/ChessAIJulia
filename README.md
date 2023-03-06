# ChessAIJulia

A university project for programming an AI for Chess using Julia

## Contents

### /Julia

This directory contains all the Jupyter Notebooks written in Julia needed for the AI.

| Notebook                | Function                                                                                     |
| ----------------------- | -------------------------------------------------------------------------------------------- |
| AlphaBetaPruning.ipynb  | **AI** that calculates a move using the Alpha-Beta-Pruning algorithm                         |
| ChessJL Summary.ipynb   | A summary of the most important methods that Chess.jl provides                               |
| EvaluatePosition.ipynb  | Evaluation a chess position refers how strong the position or one move is                    |
| IterativeDeepening.ipynb| **AI** that calculates a move using iterative deepening with the alpha-beta-pruning algorithm|
| Minimax.ipynb           | **AI** that calculates a move using the minimax algorithm                                    |
| PGN_Export_.ipynb       | Export games as PGN files                                                                    |
| PGN_Import_.ipynb       | Import PGN files as Games                                                                    |
| Play.ipynb              | **Play** as a user against one of the chess                                                  |
| Random Chess.ipynb      | **AI** that plays a random move out of a List of all possible moves using a seed             |
| ValidateUserInput.ipynb | Check is the user input in legal moves                                                       |
| ZobristHashing.ipynb    | Hashing of any Board into a unique 64-Bit Int                                                |
| style.css               | Contains some css for using the whole width of a notebook                                    |

The notebooks ending on `[notebook]_testing.ipynb` are tests for the corresponding notebook.

### /Games
This directory contains PGN (Portable Game Notation) files of chess games played against written AIs in the `Play.ipynb`. They will be saved to later on find errors to see how the chess AIs behaved.

### example_positions.txt
A text document containing chess positions in Forsyth–Edwards Notation (FEN) sorted by a meaning for testing. E.g. Positions with an obvious best move, Positions where black gets checkmated, etc.

## Reading order of the notebooks
To understand this project you will need to read the content of the notebooks. This section will give you a logical order in which the notebooks can be read.

To begin with, you will need to make yourself familiar with the `Chess.jl` library, which will be heavily used during the whole project. To get an overview of all important functions of the `Chess.jl` library you can read the `ChessJL Summary.ipynb` as well as [the official documentation of Chess.jl](https://romstad.github.io/Chess.jl/dev/).

After this you should be reading into the `EvaluatePosition.ipynb` which implements a functions to evaluate/estimate a chess position without calculating any moves into the future. This is our heuristic function ([Simplified Evaluation function](https://www.chessprogramming.org/Simplified_Evaluation_Function)) and is based on the article of Tomasz Michniewski.

After this you can read into the different AIs. The simplest AI is the Random Move AI which is implemented in the `Random Chess.ipynb` notebook. The next step is the `Minimax` Algorithm implemented in the `Minimax.ipynb` notebook. The Minimax Algorithm can be improved by using Alpha-Beta-Pruning. This is implemented in the `AlphaBetaPruning.ipynb`. Lastly, Alpha-Beta-Pruning can be improved using the `Iterative Deepening` strategy which is implemented in the `IterativeDeepening.ipynb` notebook.

The reading order of the AIs therefore should be: `Random Chess.ipynb` > `Minimax.ipynb` > `AlphaBetaPruning.ipynb` > `IterativeDeepening.ipynb`

The topic of `Memoization` is implemented in each of the AI notebooks individually. To further understand Memoization a Hashing function is needed. Therefore we use `Zobrist Hashing` implemented in `ZobristHashing.ipynb`. This notebook can be read at any time as this will not effect the understanding of the AI Algorithms.

To play with an AI you can use the `Play.ipynb` notebook. The Play.ipynb uses three notebooks which contain helpng functions included in the `ValidateUserInput.ipynb`, `PGN_Export.ipynb` and `PGN_Import.ipynb`.