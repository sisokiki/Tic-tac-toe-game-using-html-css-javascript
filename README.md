# Tic-Tac-Toe Game 🎮

A sleek and responsive Tic-Tac-Toe web application built with HTML5, CSS3, and Vanilla JavaScript.

## 🚀 Features
- **Two-Player Gameplay:** Players take turns as "O" and "X".
- **Win Detection:** Automatically identifies the winner based on horizontal, vertical, or diagonal patterns.
- **Draw Logic:** Detects when all 9 boxes are filled without a winner and declares a draw.
- **Interactive UI:** Smooth transitions and a dedicated message container to announce game results.
- **Game Controls:** Includes "Reset" and "New Game" buttons to clear the board and start over.

## 🛠️ Technologies Used
- **HTML5:** For the structured layout of the game grid and message overlays.
- **CSS3:** For styling, including Flexbox centering, custom colors, and responsive units (`vmin`).
- **JavaScript (ES6):** For the core game engine, DOM manipulation, and event handling.

## 📂 File Structure
- `index.html`: Contains the game structure and the 3x3 grid.
- `style.css`: Handles the visual design, including the bisque-colored buttons and layout.
- `app.js`: Contains the logic for checking winners and managing player turns.

## 🎮 How to Play
1. The game starts with Player "O".
2. Click on any square in the grid to place your mark.
3. The first player to get three of their marks in a row (up, down, across, or diagonally) is the winner.
4. If all nine squares are full and no player has three marks in a row, the game ends in a draw.
5. Click **"Reset Game"** or **"New Game"** to play again!

## 🧠 Logic Breakdown
The game identifies winners by iterating through a `winPatterns` array that contains the indices of the grid:
```javascript
let winPatterns = [
  [0, 1, 2], [3, 4, 5], [6, 7, 8], // Rows
  [0, 3, 6], [1, 4, 7], [2, 5, 8], // Columns
  [0, 4, 8], [2, 4, 6]             // Diagonals
];
