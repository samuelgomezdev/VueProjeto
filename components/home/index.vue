<template>
    <div class="home">
      <header>
        <h1>Bem-vindo à Home!</h1>
      </header>
      
      <main>
        <p>Este é um exemplo de uma página inicial simples em Vue.js.</p>
        <button @click="showMessage">Clique aqui</button>
        <p v-if="message">{{ message }}</p>
      </main>
      
      <footer>
        <p>&copy; 2024 Jean Paulo</p>
      </footer>
    </div>
  </template>
  
  <script>
  export default {
    name: "Home",
    data() {
      return {
        message: "",
      };
    },
    methods: {
      showMessage() {
        this.message = "Você clicou no botão!";
      },
    },
  };
  </script>
  
  <style scoped>
  .home {
    text-align: center;
    font-family: Arial, sans-serif;
    color: #333;
  }
  
  header {
    background-color: #4CAF50;
    color: white;
    padding: 20px;
  }
  
  main {
    padding: 20px;
  }
  
  footer {
    background-color: #f1f1f1;
    color: #555;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
  }
  </style>
  