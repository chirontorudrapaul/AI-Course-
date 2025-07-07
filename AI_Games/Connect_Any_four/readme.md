# **Connect Four Game with Minimax AI**

A classic Connect Four game implemented in Python using Pygame, where you can play against an AI opponent powered by the Minimax algorithm with Alpha-Beta pruning.

---

## **i. How to Run Your File**

### **Navigate to the Game Folder**

cd AI-Course/AI_Games/Connect_Any_Four

### **Run the Game**
Execute the Python script:

python connect_four.py

## **ii. Software/Library/Framework Requirements**

- **Python**: Version 3.8 or higher
- **NumPy**: For efficient numerical operations
 
         pip install numpy

- **Pygame**: For rendering the game UI
 
         pip install pygame


## **iii. How to Play the Game**

### **Start the Game**
Run the script as described above. A menu screen will appear with options:

- Press **`1`** to play as **Red (Player)** and go first
- Press **`2`** to play as **Yellow (AI)** and go second
- Press **`Q`** to quit

### **Gameplay**

**Player's Turn (Red):**
- Move your mouse horizontally to see a preview of your disc
- Click on the column where you want to drop your disc

**AI's Turn (Yellow):**
- The AI will automatically calculate the best move using the Minimax algorithm and drop its disc

### **Winning Condition**
Connect four discs horizontally, vertically, or diagonally to win

### **Game Over**
- If you or the AI wins, a message will display on the screen
- You will be prompted to play again:
  - Press **`Y`** to restart
  - Press **`N`** to exit

---

## **iv. Screenshots of the Game**

Here are some visuals of the game:

### **Menu Screen**

### **Gameplay - Player's Turn**


### **Gameplay - AI's Turn**


### **Winning Screen - Player / AI Wins**


## **v. Algorithm Used**

The AI opponent in this game uses the **Minimax Algorithm with Alpha-Beta Pruning**.

### **How Minimax Works:**
- **Maximizing Player (AI)**: Tries to maximize its chances of winning (score)
- **Minimizing Player (Human)**: Tries to minimize the AI's chances of winning
- **Depth-Limited Search**: The AI looks ahead 5 moves (`depth = 5`) to evaluate the best move
- **Evaluation Function**: Scores the board based on:
  - Center control
  - Potential winning moves
  - Blocking opponent's winning moves
- **Alpha-Beta Pruning**: Optimizes the search by skipping irrelevant branches

### **Key Functions:**
- `minimax(board, depth, alpha, beta, maximizingPlayer)`: Implements the Minimax logic
- `score_position(board, piece)`: Evaluates the board's state for a given player
- `winning_move(board, piece)`: Checks if the current player has won

This algorithm ensures the AI is:
- **Unbeatable** at depth 5 (hard difficulty)
- **Fast** due to Alpha-Beta pruning (avg. move time < 1s)
