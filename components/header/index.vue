<template>
    <header class="header">
      <nav class="navbar">
        <div class="logo">
          <a href="/">MinhaLogo</a>
        </div>
        <ul class="nav-links" :class="{ active: isMenuOpen }">
          <li><a href="#home">Home</a></li>
          <li><a href="#about">Sobre</a></li>
          <li><a href="#services">Serviços</a></li>
          <li><a href="#contact">Contato</a></li>
        </ul>
        <button class="menu-toggle" @click="toggleMenu">
          <span class="hamburger"></span>
        </button>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isMenuOpen: false,
      };
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen;
      },
    },
  };
  </script>
  
  <style scoped>
  /* Estilo básico do header */
  .header {
    width: 100%;
    background-color: #333;
    color: #fff;
  }
  
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
  }
  
  .logo a {
    color: #fff;
    font-size: 1.5rem;
    text-decoration: none;
    font-weight: bold;
  }
  
  .nav-links {
    list-style: none;
    display: flex;
    gap: 1.5rem;
  }
  
  .nav-links li a {
    color: #fff;
    text-decoration: none;
    font-size: 1rem;
  }
  
  .nav-links.active {
    display: block;
  }
  
  .menu-toggle {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
  }
  
  .menu-toggle .hamburger {
    width: 25px;
    height: 3px;
    background-color: #fff;
    position: relative;
  }
  
  .menu-toggle .hamburger::before,
  .menu-toggle .hamburger::after {
    content: "";
    width: 25px;
    height: 3px;
    background-color: #fff;
    position: absolute;
    left: 0;
    transition: 0.3s;
  }
  
  .menu-toggle .hamburger::before {
    top: -8px;
  }
  
  .menu-toggle .hamburger::after {
    top: 8px;
  }
  
  /* Estilo para dispositivos móveis */
  @media (max-width: 768px) {
    .nav-links {
      flex-direction: column;
      gap: 1rem;
      display: none;
      position: absolute;
      top: 100%;
      left: 0;
      width: 100%;
      background-color: #333;
      padding: 1rem 0;
    }
  
    .nav-links.active {
      display: flex;
    }
  
    .menu-toggle {
      display: block;
    }
  }
  </style>
  