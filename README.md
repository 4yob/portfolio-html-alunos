# Projeto Portfólio HTML & CSS

Projeto de um portfólio simples feito com HTML e CSS.

## Tecnologias

- HTML
- CSS

## Passos de criação

1. Criação do arquivo `index.html` com a estrutura básica do HTML
2. Criação do arquivo `assets/styles.css` com o estilo inicial do projeto

```css
* {
  margin: 0; /* Remove a margem padrão do body que é 8px */
  padding: 0; /* Remove o padding padrão do body que é 8px */
  box-sizing: border-box; /* Faz com que o padding e a borda não aumentem o tamanho do elemento */
  text-decoration: none; /* Remove o sublinhado dos links */
  border: none; /* Remove a borda padrão dos elementos */
  outline: none; /* Remove a borda de foco dos elementos */
  scroll-behavior: smooth; /* Adiciona um efeito de rolagem suave */
  font-family: "Poppins", sans-serif; /* Define a fonte padrão do projeto */
}

:root {
  --bg-color: #080808; /* Define a cor de fundo do projeto */
  --secondary-bg-color: #121212; /* Define a cor de fundo secundária do projeto */
  --text-color: #fff; /* Define a cor do texto do projeto */
  --main-color: #00ffee; /* Define a cor principal do projeto */
}

html {
  overflow-x: hidden; /* Remove a barra de rolagem horizontal */
}

body {
  background-color: var(--bg-color); /* Define a cor de fundo do body */
  color: var(--text-color); /* Define a cor do texto do body */
}
```

3. Link do arquivo CSS no arquivo HTML e da biblioteca de ícones (Boxicons)
4. Criação da header do projeto

```html
<header class="header">
  <a href="#home" class="logo">Felipe <span>Santos</span></a>

  <nav class="navbar">
    <a href="#home" class="active">Início</a>
    <a href="#education">Acadêmico</a>
    <a href="#services">Serviços</a>
    <a href="#testimonials">Depoimentos</a>
    <a href="#contact">Contato</a>
  </nav>
</header>
```

```css
.header {
  position: fixed; /* Fixa o cabeçalho no topo da página */
  top: 0; /* Define a distância do topo */
  left: 0; /* Define a distância da esquerda */
  width: 100%; /* Define a largura do cabeçalho */
  padding: 2rem 10rem; /* Adiciona um espaçamento interno */
  background: rgba(0, 0, 0, 0.3); /* Adiciona um fundo com transparência */
  backdrop-filter: blur(10px); /* Adiciona um efeito de desfoque */
  display: flex; /* Faz com que os elementos fiquem em linha */
  justify-content: space-between; /* Alinha os elementos no espaço entre eles */
  align-items: center; /* Alinha os elementos no centro no eixo vertical */
  z-index: 5; /* Define a ordem de empilhamento */
}

.logo {
  font-size: 2rem; /* Define o tamanho da fonte equivalente a 48px */
  color: var(--text-color);
  font-weight: 800; /* Define o peso da fonte */
  cursor: pointer; /* Adiciona um cursor de ponteiro */
  transition: 0.3s ease; /* Adiciona uma transição suave */
}

.logo:hover {
  transform: scale(1.03); /* Adiciona um efeito de escala */
}

.logo span {
  text-shadow: 0 0 5px var(--main-color); /* Adiciona uma sombra no texto */
}

.navbar a {
  font-size: 1.2rem; /* Define o tamanho da fonte equivalente a 16px */
  color: var(--text-color);
  margin-left: 4rem; /* Adiciona uma margem à esquerda */
  font-weight: 500; /* Define o peso da fonte */
  transition: 0.3s ease; /* Adiciona uma transição suave */
  border-bottom: 3px solid transparent; /* Adiciona uma borda na parte inferior */
  border-radius: 3px; /* Adiciona um raio nas bordas */
}

.navbar a:hover,
.navbar a.active {
  color: var(--main-color); /* Define a cor do texto */
  border-bottom: 3px solid var(--main-color); /* Adiciona uma borda na parte inferior */
  border-radius: 3px; /* Adiciona um raio nas bordas */
}
```

5. Criação da seção home do projeto

```html
<section class="home" id="home">
  <div class="home-content">
    <h1>Olá, eu sou <span>Felipe Dev</span></h1>
    <h3 class="text-animation">Sou um <span></span></h3>
    <p>
      Desenvolvedor Fullstack com experiência em desenvolvimento de aplicações
      web e mobile. Entre em contato para saber mais.
    </p>

    <div class="social-icons">
      <a href="#" target="_blank"><i class="bx bxl-github"></i></a>
      <a href="#" target="_blank"><i class="bx bxl-linkedin"></i></a>
      <a href="#" target="_blank"><i class="bx bxl-twitter"></i></a>
      <a href="#" target="_blank"><i class="bx bxl-discord-alt"></i></a>
    </div>

    <div class="btn-group">
      <a href="#hire" class="btn">Contrate-me</a>
      <a href="#contact" class="btn">Contato</a>
    </div>
  </div>

  <div class="home-img">
    <img
      src="https://github.com/FelipeSantos92Dev.png"
      alt="Pessoa olhando para trás usando boné"
    />
  </div>
</section>
```

```css
section {
  min-height: 100vh; /* Define a altura mínima da seção */
  padding: 10rem; /* Adiciona um espaçamento interno */
}

.home {
  display: flex; /* Faz com que os elementos fiquem em linha */
  align-items: center; /* Alinha os elementos no centro no eixo vertical */
  justify-content: center; /* Alinha os elementos no centro no eixo horizontal */
  gap: 16rem; /* Adiciona um espaçamento entre os elementos */
}

.home-content {
  display: flex; /* Faz com que os elementos fiquem em linha */
  flex-direction: column; /* Alinha os elementos em coluna */
  align-items: baseline; /* Alinha os elementos na base */
  text-align: left; /* Alinha o texto à esquerda */
  justify-content: center; /* Alinha os elementos no centro no eixo horizontal */
  margin-top: 3rem; /* Adiciona uma margem no topo */
}

span {
  color: var(--main-color); /* Define a cor do texto */
}

.logo span {
  color: var(--main-color); /* Define a cor do texto */
}

.home-content h3 {
  margin-top: 1rem; /* Adiciona uma margem na parte superior */
  margin-bottom: 2rem; /* Adiciona uma margem na parte inferior */
  font-size: 2rem; /* Define o tamanho da fonte equivalente a 56px */
}

.home-content h1 {
  font-size: 4rem; /* Define o tamanho da fonte equivalente a 112px */
  font-weight: 700; /* Define o peso da fonte */
  margin-top: 1.5rem; /* Adiciona uma margem na parte superior */
  line-height: 1; /* Define a altura da linha */
}

.home-img {
  border-radius: 50%; /* Adiciona um raio nas bordas */
}

.home-img img {
  position: relative; /* Define a posição relativa ao elemento anterior */
  top: 3rem; /* Define a distância do topo */
  width: 20vw; /* Define a largura do elemento equivalente a 32% da largura da tela */
  border-radius: 50%; /* Adiciona um raio nas bordas */
  box-shadow: 0 0 20px var(--main-color); /* Adiciona uma sombra */
  cursor: pointer; /* Adiciona um cursor de ponteiro */
  transition: 0.4s ease-in-out; /* Adiciona uma transição suave */
}

.home-img img:hover {
  box-shadow: 0 0 20px var(--main-color), 0 0 40px var(--main-color),
    0 0 60px var(--main-color); /* Adiciona uma sombra */
}

.home-content p {
  font-size: 1.2rem; /* Define o tamanho da fonte equivalente a 16px */
  font-weight: 400; /* Define o peso da fonte */
  line-height: 1.6; /* Define a altura da linha */
  max-width: 1000px; /* Define a largura máxima do elemento */
}

.social-icons a {
  display: inline-flex; /* Faz com que os elementos fiquem em linha com a mesma altura */
  justify-content: center; /* Alinha os elementos no centro no eixo horizontal */
  align-items: center; /* Alinha os elementos no centro no eixo vertical */
  width: 4rem; /* Define a largura do elemento */
  height: 4rem; /* Define a altura do elemento */
  background: transparent; /* Define o fundo transparente */
  border: 2px solid var(--main-color); /* Adiciona uma borda */
  font-size: 2.5rem; /* Define o tamanho da fonte equivalente a 40px */
  border-radius: 50%; /* Adiciona um raio nas bordas */
  color: var(--main-color); /* Define a cor do texto */
  margin: 2rem 1.5rem 2rem 0; /* Adiciona uma margem */
  transition: 0.3s ease-in-out; /* Adiciona uma transição suave */
}

.social-icons a:hover {
  color: var(--text-color); /* Define a cor do texto */
  transform: scale(1.1) translateY(-2px); /* Adiciona um efeito de escala no eixo Y */
  box-shadow: 0 0 25px var(--main-color); /* Adiciona uma sombra */
  background-color: var(--main-color); /* Define a cor de fundo */
}

.btn {
  display: inline-block; /* Faz com que o elemento seja exibido em linha */
  padding: 1rem 2rem; /* Adiciona um espaçamento interno */
  background: var(--main-color); /* Define a cor de fundo */
  box-shadow: 0 0 20px var(--main-color); /* Adiciona uma sombra */
  border-radius: 5px; /* Adiciona um raio nas bordas */
  font-size: 1.2rem; /* Define o tamanho da fonte equivalente a 16px */
  color: var(--bg-color); /* Define a cor do texto */
  border: 2px solid transparent; /* Adiciona uma borda */
  letter-spacing: 0.1rem; /* Define o espaçamento entre as letras */
  font-weight: 500; /* Define o peso da fonte */
  transition: 0.3s ease-in-out; /* Adiciona uma transição suave */
  cursor: pointer; /* Adiciona um cursor de ponteiro */
}

.btn:hover {
  transform: scale(1.05); /* Adiciona um efeito de escala */
  box-shadow: 0 0 10px var(--main-color), 0 0 15px var(--main-color),
    0 0 20px var(--main-color); /* Adiciona uma sombra */
}

.btn-group {
  display: flex; /* Faz com que os elementos fiquem em linha */
  align-items: center; /* Alinha os elementos no centro no eixo vertical */
  gap: 1.5rem; /* Adiciona um espaçamento entre os elementos */
}

.btn-group a:nth-of-type(2) {
  /* Seleciona o segundo elemento do grupo */
  background-color: var(--bg-color); /* Define a cor de fundo */
  color: var(--main-color); /* Define a cor do texto */
  border: 2px solid var(--main-color); /* Adiciona uma borda */
  box-shadow: 0 0 20px transparent; /* Adiciona uma sombra */
}

.btn-group a:nth-of-type(2):hover {
  box-shadow: 0 0 20px var(--main-color); /* Adiciona uma sombra */
  background-color: var(--main-color); /* Define a cor de fundo */
  color: var(--bg-color); /* Define a cor do texto */
}
```

6. Animação do texto da seção home

```css
.text-animation {
  font-size: 34px; /* Define o tamanho da fonte */
  font-weight: 600; /* Define o peso da fonte */
  min-width: 280px; /* Define a largura mínima */
}

.text-animation span {
  position: relative; /* Define a posição relativa */
}

.text-animation span::before {
  content: "Desenvolvedor Fullstack"; /* Adiciona um conteúdo */
  color: var(--main-color); /* Define a cor do texto */
  animation: words 20s infinite; /* Adiciona uma animação */
}

.text-animation span::after {
  content: ""; /* Adiciona um conteúdo vazio */
  background-color: var(--bg-color); /* Define a cor de fundo */
  position: absolute; /* Define a posição absoluta */
  width: calc(100% + 8px); /* Define a largura de acordo com o conteúdo */
  height: 100%; /* Define a altura de acordo com o conteúdo */
  border-left: 3px solid var(--bg-color); /* Adiciona uma borda à esquerda */
  right: -8px; /* Define a distância da direita */
  animation: cursor 1s infinite, typing 20s steps(14) infinite; /* Adiciona uma animação que simula um cursor */
}

@keyframes cursor {
  /* Define a animação do cursor */
  to {
    border-left: 3px solid var(--main-color); /* Adiciona uma borda à esquerda */
  }
}

@keyframes words {
  /* Define a animação das palavras */
  0%,
  20% {
    content: "Desenvolvedor Frontend"; /* Adiciona um conteúdo */
  }
  21%,
  40% {
    content: "Desenvolvedor Backend"; /* Adiciona um conteúdo */
  }
  41%,
  60% {
    content: "Desenvolvedor Mobile"; /* Adiciona um conteúdo */
  }
  61%,
  80% {
    content: "Desenvolvedor Web"; /* Adiciona um conteúdo */
  }
  81%,
  100% {
    content: "Desenvolvedor Fullstack"; /* Adiciona um conteúdo */
  }
}

@keyframes typing {
  /* Define a animação da digitação */
  10%,
  15%,
  30%,
  35%,
  50%,
  55%,
  70%,
  75%,
  90%,
  95% {
    width: 0; /* Define a largura como zero */
  }
  5%,
  20%,
  25%,
  40%,
  45%,
  60%,
  65%,
  80%,
  85%,
  100% {
    width: calc(100% + 8px); /* Define a largura de acordo com o conteúdo */
  }
}
```

7. Criação da seção de formação acadêmica

```html
<section class="education" id="education">
  <h2 class="heading">Acadêmico</h2>

  <div class="timeline-items">
    <div class="timeline-item">
      <div class="timeline-dot">
        <div class="timeline-date">2024</div>
        <div class="timeline-content">
          <h3>Pós-graduação | Gestão de Projetos em TI</h3>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laboriosam
            recusandae totam, magni cumque iste dignissimos iure dicta,
            repudiandae eos sequi reprehenderit ducimus amet voluptate? Eos
            tempora labore facere obcaecati sapiente.
          </p>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot">
        <div class="timeline-date">2022</div>
        <div class="timeline-content">
          <h3>Pós-graduação | Engenharia de Software</h3>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laboriosam
            recusandae totam, magni cumque iste dignissimos iure dicta,
            repudiandae eos sequi reprehenderit ducimus amet voluptate? Eos
            tempora labore facere obcaecati sapiente.
          </p>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot">
        <div class="timeline-date">2021</div>
        <div class="timeline-content">
          <h3>Graduação | Análise e Desenvolvimento de Sistemas</h3>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laboriosam
            recusandae totam, magni cumque iste dignissimos iure dicta,
            repudiandae eos sequi reprehenderit ducimus amet voluptate? Eos
            tempora labore facere obcaecati sapiente.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
```

```css
.heading {
  font-size: 2rem; /* Define o tamanho da fonte equivalente a 40px */
  text-align: center; /* Alinha o texto ao centro */
  margin: 5rem 0; /* Adiciona uma margem */
}

.education {
  padding: 100px 15px; /* Adiciona um espaçamento interno */
  background: var(--secondary-bg-color); /* Define a cor de fundo */
}

.education h2 {
  margin-bottom: 5rem; /* Adiciona uma margem na parte inferior */
}

.timeline-items {
  max-width: 1200px; /* Define a largura máxima */
  margin: auto; /* Adiciona uma margem automática */
  display: flex; /* Faz com que os elementos fiquem em linha */
  flex-wrap: wrap; /* Quebra a linha quando não há espaço */
  position: relative; /* Define a posição relativa */
}

.timeline-items::before {
  /* Adiciona um pseudo-elemento */
  content: ""; /* Adiciona um conteúdo vazio */
  position: absolute; /* Define a posição absoluta */
  width: 5px; /* Define a largura */
  height: 100%; /* Define a altura */
  background-color: var(--main-color); /* Define a cor de fundo */
  left: calc(50% - 1px); /* Define a distância da esquerda */
  top: 0; /* Define a distância do topo */
  transform: translateX(-50%); /* Adiciona um efeito de translação */
}

.timeline-item {
  margin-bottom: 40px; /* Adiciona uma margem */
  width: 100%; /* Define a largura */
  position: relative; /* Define a posição relativa */
}

.timeline-item:last-child {
  /* Seleciona o último elemento */
  margin-bottom: 0; /* Remove a margem */
}

.timeline-item:nth-child(odd) {
  /* Seleciona os elementos ímpares */
  padding-right: calc(50% + 30px); /* Adiciona um espaçamento à direita */
  text-align: right; /* Alinha o texto à direita */
}

.timeline-item:nth-child(even) {
  /* Seleciona os elementos pares */
  padding-left: calc(50% + 30px); /* Adiciona um espaçamento à esquerda */
  text-align: left; /* Alinha o texto à esquerda */
}

.timeline-dot {
  height: 21px; /* Define a altura */
  width: 21px; /* Define a largura */
  background-color: var(--main-color); /* Define a cor de fundo */
  box-shadow: 0 0 20px var(--main-color), 0 0 30px var(--main-color); /* Adiciona uma sombra */
  position: absolute; /* Define a posição absoluta */
  left: calc(50% - 11px); /* Define a distância da esquerda */
  border-radius: 50%; /* Adiciona um raio nas bordas */
}

.timeline-date {
  font-size: 1.6rem; /* Define o tamanho da fonte equivalente a 16px */
  font-weight: 800; /* Define o peso da fonte */
  color: var(--text-color); /* Define a cor do texto */
  margin: 0 0 15px; /* Adiciona uma margem */
}

.timeline-content {
  background: var(--bg-color); /* Define a cor de fundo */
  border: 1px solid var(--main-color); /* Adiciona uma borda */
  padding: 30px 50px; /* Adiciona um espaçamento interno */
  border-radius: 5px; /* Adiciona um raio nas bordas */
  box-shadow: 0 0 10px var(--main-color); /* Adiciona uma sombra */
  cursor: pointer; /* Adiciona um cursor de ponteiro */
  transition: 0.3s ease-in-out; /* Adiciona uma transição suave */
}

.timeline-content:hover {
  transform: scale(1.05); /* Adiciona um efeito de escala */
  box-shadow: 0 0 20px var(--main-color); /* Adiciona uma sombra */
}

.timeline-content h3 {
  font-size: 1.6rem; /* Define o tamanho da fonte equivalente a 16px */
  font-weight: 600; /* Define o peso da fonte */
  color: var(--text-color); /* Define a cor do texto */
  margin: 0 0 10px; /* Adiciona uma margem */
}

.timeline-content p {
  font-size: 1.2rem; /* Define o tamanho da fonte equivalente a 16px */
  font-weight: 300; /* Define o peso da fonte */
  color: var(--text-color); /* Define a cor do texto */
  line-height: 1.2; /* Define a altura da linha */
}
```
