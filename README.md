# Checkers AI Duel

## Overview

This project is a PyQt5-powered GUI application that lets two AI “bots” play a full game of Checkers against each other. You can select between two evaluation strategies (`group1` vs. `group2`) for each bot and watch them battle it out on a custom board.

- **Bot Strategies**  
  - `group1`: A heuristic evaluator that scores moves based on piece value, mobility, and endgame/midgame stage :contentReference[oaicite:0]{index=0}:contentReference[oaicite:1]{index=1}.  
  - `group2`: A baseline random-move selector for comparison :contentReference[oaicite:2]{index=2}:contentReference[oaicite:3]{index=3}.  
- **GUI**  
  - Launches a window with two panels (Purple Bot vs. Grey Bot), algorithm selectors, and a “Play” button.  
  - Renders a custom background and piece graphics.  
- **Game Loop**  
  - Alternating turns until no more moves are available.  
  - Prints total execution time when the game ends.

## Features

- **Dynamic Strategy Loading**  
  Uses Python’s `importlib` to load `group1` and `group2` functions at runtime from their respective `.py` files :contentReference[oaicite:4]{index=4}:contentReference[oaicite:5]{index=5}.  
- **Heuristic Evaluation**  
  `evaluate_Move` in `checkers.py` weighs material, future mobility, opponent mobility, and game stage.  
- **Simple Baseline**  
  `group2` picks a random legal move to serve as a control strategy.  
- **Clean GUI**  
  Built with PyQt5 for smooth rendering of the board, pieces, and controls.

## Requirements

- Python 3.7 or higher  
- PyQt5  
- pygame (for any sound effects or future extensions)  

All dependencies are listed in `requirements.txt`.
