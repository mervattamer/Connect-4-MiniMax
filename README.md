# Connect 4 Game

Connect 4 is a classic two-player game where players strategically drop colored discs into a grid, aiming to connect four of their own discs vertically, horizontally, or diagonally. This project provides a full game with a graphical user interface (GUI) featuring a human-vs-computer mode. In this mode, players can choose whether to use alpha-beta pruning in the AI agent.

## Game Rules

- **Players:** Two (Human vs. Computer)
- **Objective:** Connect four discs of the same color vertically, horizontally, or diagonally.
- **Gameplay:** Players take turns dropping their colored discs from the top into a grid. Discs fall straight down to occupy the next available space within the column.
- **Winning:** The game continues until the board is full. The player with a greater number of connected fours wins.

## Game Dimensions

- **Width:** ≥ 7
- **Length:** ≥ 6

## AI Algorithms

The game supports the following AI algorithms as options for the computer opponent:

1. **Minimax without Alpha-Beta Pruning**
2. **Minimax with Alpha-Beta Pruning**
3. **Expected Minimax**
   - Probability that a disc falls in the chosen column is 0.6.
   - Probability that it falls into the column on the left or right is 0.4.

## Heuristic Function and Truncation

Due to the immense size of the full game tree (O(10^35)), it is impractical to traverse it to terminal states. Therefore, a heuristic function is implemented to evaluate the state of the game. The function returns a number indicating whether the computer is near to winning or losing. The game tree is truncated after K levels, and players can set the parameter K before starting the game.

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/mervattamer/Connect-4-MiniMax.git
   cd Connect-4-MiniMax
   ```

2. **Install Dependencies:**
   ```bash
   # Install Pygame
    pip install pygame

   # Install NumPy
    pip install numpy

3. **Run the Game:**
   ```bash
   python connect4.py
   ```

## Options

- **Human vs. Computer:** Choose the player color and AI algorithm.
- **Set K parameter:** Adjust the depth for truncating the game tree.


## Contributing

Feel free to contribute by submitting bug reports, feature requests, or code contributions.



## Acknowledgments

Thanks to the creators of Connect 4 for the classic game inspiration!

---
