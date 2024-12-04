<template>
    <div class="tic-tac-toe">
      <h1>Jogo da Velha</h1>
      <div class="board">
        <div
          v-for="(cell, index) in board"
          :key="index"
          class="cell"
          :class="{ filled: cell }"
          @click="makeMove(index)"
        >
          {{ cell }}
        </div>
      </div>
      <p v-if="winner" class="message">{{ winnerMessage }}</p>
      <p v-if="isDraw && !winner" class="message">Empate!</p>
      <button @click="resetGame" class="reset-button">Reiniciar Jogo</button>
    </div>
  </template>
  
  <script>
  export default {
    name: "TicTacToe",
    data() {
      return {
        board: Array(9).fill(""),
        currentPlayer: "X",
        winner: null,
        isDraw: false,
      };
    },
    computed: {
      winnerMessage() {
        return this.winner ? `Jogador ${this.winner} venceu!` : "";
      },
    },
    methods: {
      makeMove(index) {
        if (!this.board[index] && !this.winner) {
          this.$set(this.board, index, this.currentPlayer);
          if (this.checkWinner()) {
            this.winner = this.currentPlayer;
          } else if (this.board.every((cell) => cell)) {
            this.isDraw = true;
          } else {
            this.currentPlayer = this.currentPlayer === "X" ? "O" : "X";
          }
        }
      },
      checkWinner() {
        const winningCombinations = [
          [0, 1, 2],
          [3, 4, 5],
          [6, 7, 8],
          [0, 3, 6],
          [1, 4, 7],
          [2, 5, 8],
          [0, 4, 8],
          [2, 4, 6],
        ];
        return winningCombinations.some((combination) => {
          const [a, b, c] = combination;
          return (
            this.board[a] &&
            this.board[a] === this.board[b] &&
            this.board[a] === this.board[c]
          );
        });
      },
      resetGame() {
        this.board = Array(9).fill("");
        this.currentPlayer = "X";
        this.winner = null;
        this.isDraw = false;
      },
    },
  };
  </script>
  
  <style scoped>
  .tic-tac-toe {
    text-align: center;
    margin-top: 20px;
  }
  
  .board {
    display: grid;
    grid-template-columns: repeat(3, 100px);
    grid-gap: 10px;
    margin: 20px auto;
  }
  
  .cell {
    width: 100px;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    font-weight: bold;
    border: 1px solid #333;
    cursor: pointer;
    background-color: #f9f9f9;
  }
  
  .cell.filled {
    cursor: not-allowed;
    background-color: #e0e0e0;
  }
  
  .message {
    font-size: 18px;
    margin: 10px 0;
  }
  
  .reset-button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .reset-button:hover {
    background-color: #0056b3;
  }
  </style>
  