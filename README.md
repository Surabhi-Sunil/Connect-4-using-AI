# Connect 4 AI – Minimax, MCTS, and Negamax Evaluation

This project evaluates the performance of three AI algorithms – Minimax (with and without a custom heuristic), Monte Carlo Tree Search (MCTS), and Negamax – applied to the Connect 4 game. The goal is to determine their effectiveness in strategic gameplay, efficiency, and adaptability.

## 📁 Files

- `AI_project.ipynb`: Main notebook implementing and comparing the AI strategies.
- `AI_REPORT.pdf`: Detailed report outlining methodology, literature review, experimental setup, and findings.

## 🎯 Objective

To implement and compare the performance of three game-playing AI algorithms and a custom heuristic:
- **Minimax (with alpha-beta pruning)**
- **Minimax with custom heuristic**
- **Negamax**
- **Monte Carlo Tree Search (MCTS)**

The agents were evaluated based on:
- Win rate against each other
- Average time per game

## 🧠 Algorithms Used

- **Minimax with Alpha-Beta Pruning**: Classic tree search algorithm optimized by pruning.
- **Minimax with Custom Heuristic**: Evaluates board states using a weighted scoring strategy.
- **Negamax**: A simplified variant of Minimax optimized for zero-sum games.
- **MCTS**: A probabilistic strategy using random simulations to determine moves.

## 🧪 Experimental Setup

Each pair of agents played multiple games (10–50 matches) with fixed depths and heuristics. The board state and winner were printed for each game. Timing functions measured performance.

## 📊 Results Summary

| Player 1         | Player 2         | Wins (P1/P2/Tie)        | Total Time (s) | Avg Time/Game (s) |
|------------------|------------------|--------------------------|----------------|-------------------|
| MCTS             | Custom Heuristic | 48 / 1 / 1               | 5304.77        | 106.10            |
| Custom Heuristic | MCTS             | 3 / 46 / 1               | 6197.38        | 123.95            |
| MCTS             | Alpha-Beta       | 49 / 0 / 1               | 2078.70        | 41.57             |
| Alpha-Beta       | MCTS             | 0 / 50 / 0               | 1830.31        | 36.61             |
| Negamax          | MCTS             | 0 / 10 / 0               | 482.53         | 48.25             |
| Negamax          | Custom Heuristic | 0 / 10 / 0               | 2213.86        | 221.39            |
| Negamax          | Alpha-Beta       | 0 / 0 / 50               | 450.31         | 9.00              |

## 🏆 Key Takeaways

- **Best Performer**: MCTS (dominated all other agents in both win rate and consistency).
- **Worst Performer**: Negamax (limited by depth = 5 and higher computational cost).
- **Heuristic Impact**: The custom heuristic enhanced decision-making over basic alpha-beta, but was still outperformed by MCTS.

## 💡 Future Work

- Improve the custom heuristic with deeper insights and patterns
- Run simulations with larger game sets
- Explore reinforcement learning and neural networks for adaptive strategies

## ⚙️ Setup Instructions (Colab)

1. **Mount Google Drive**:
    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```

2. **Clone AIMA Repository**:
    ```bash
    !git clone https://github.com/aimacode/aima-python.git
    ```

3. **Install Dependencies**:
    ```bash
    %cd aima-python
    !pip install -r requirements.txt
    ```

4. **Run `AI_project.ipynb`**: Follow the notebook cells to test each algorithm.

---

**Authors**: Surabhi Sunil, Chinmayee Dharmastalam Sreedhar  
**Course**: CSci 5511  
**Date**: December 2024  
**License**: MIT (inherits from AIMA-Python)
