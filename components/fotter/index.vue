<template>
    <footer class="footer">
      <div class="container">
        <div class="footer-section">
          <h4>Sobre Nós</h4>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero.</p>
        </div>
        <div class="footer-section">
          <h4>Links Rápidos</h4>
          <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">Sobre</a></li>
            <li><a href="#services">Serviços</a></li>
            <li><a href="#contact">Contato</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Fale Conosco</h4>
          <p>Email: contato@exemplo.com</p>
          <p>Telefone: (11) 1234-5678</p>
          <div class="social-icons">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 Minha Empresa. Todos os direitos reservados.</p>
      </div>
    </footer>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style scoped>
  /* Estilo geral do footer */
  .footer {
    background-color: #333;
    color: #fff;
    padding: 2rem 0;
    text-align: center;
  }
  
  .container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 1rem;
    padding: 0 2rem;
  }
  
  .footer-section {
    flex: 1 1 30%;
    min-width: 200px;
  }
  
  .footer-section h4 {
    margin-bottom: 1rem;
    font-size: 1.2rem;
    color: #f4f4f4;
  }
  
  .footer-section p,
  .footer-section ul {
    font-size: 0.9rem;
    color: #ccc;
  }
  
  .footer-section ul {
    list-style: none;
    padding: 0;
  }
  
  .footer-section ul li {
    margin-bottom: 0.5rem;
  }
  
  .footer-section ul li a {
    color: #ccc;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .footer-section ul li a:hover {
    color: #fff;
  }
  
  .social-icons a {
    margin: 0 0.5rem;
    font-size: 1.2rem;
    color: #ccc;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  .social-icons a:hover {
    color: #fff;
  }
  
  .footer-bottom {
    margin-top: 2rem;
    font-size: 0.8rem;
    color: #aaa;
  }
  
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
      align-items: center;
    }
  
    .footer-section {
      text-align: center;
    }
  }
  </style>
  