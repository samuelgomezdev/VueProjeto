<template>
  <div class="home">
    <header class="hero">
      <h1 class="hero-title">Olá, eu sou <span class="highlight">[Seu Nome]</span></h1>
      <p class="hero-subtitle">
        Desenvolvedor apaixonado por criar soluções inovadoras e elegantes para a web.
      </p>
    </header>

    <section class="about">
      <h2 class="section-title">Sobre Mim</h2>
      <p class="about-text">
        Sou um desenvolvedor com experiência em front-end e back-end, especializado em 
        tecnologias como JavaScript, Vue.js, Node.js e muito mais. Minha missão é transformar 
        ideias em projetos funcionais e esteticamente agradáveis.
      </p>
    </section>

    <section class="skills">
      <h2 class="section-title">Minhas Habilidades</h2>
      <ul class="skills-list">
        <li>Desenvolvimento Front-End</li>
        <li>Desenvolvimento Back-End</li>
        <li>Criação de APIs RESTful</li>
        <li>Integração com serviços de terceiros</li>
        <li>UI/UX Design</li>
      </ul>
    </section>


  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style>
/* Estilo global */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background: #f4f4f9;
  color: #333;
}

.home {
  text-align: center;
  padding: 20px;
}

/* Hero Section */
.hero {
  background: linear-gradient(to right, #4facfe, #00f2fe);
  color: #fff;
  padding: 50px 20px;
  margin-bottom: 30px;
}

.hero-title {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.highlight {
  color: #ffdd57;
}

.hero-subtitle {
  font-size: 1.2rem;
}

/* About Section */
.about {
  margin: 20px auto;
  max-width: 800px;
}

.section-title {
  font-size: 2rem;
  margin-bottom: 15px;
  color: #4facfe;
}

.about-text {
  font-size: 1.1rem;
  line-height: 1.6;
}

/* Skills Section */
.skills {
  margin: 20px auto;
  max-width: 800px;
}

.skills-list {
  list-style: none;
  padding: 0;
}

.skills-list li {
  font-size: 1.1rem;
  padding: 5px 0;
  border-bottom: 1px solid #ddd;
}

/* Footer */
.footer {
  margin-top: 40px;
  padding: 20px;
  background: #333;
  color: #fff;
}

.footer-text a {
  color: #4facfe;
  text-decoration: none;
}

.footer-text a:hover {
  text-decoration: underline;
}
</style>
