<script setup>
import { ref } from 'vue';
const paginaAtual = ref("home"); 

function irParaLogin() {
  paginaAtual.value = "login";
}
function irParaCriarEmpresas() {
  paginaAtual.value = "criarEmpresas";
}
function irParaCriarFormado() {
  paginaAtual.value = "criarFormado";
}
function irParaLoginFormado() {
  paginaAtual.value = "LoginFormado";
}
function irParaLoginEmpresa() {
  paginaAtual.value = "LoginEmpresa";
}
function irParaHome() {
  paginaAtual.value = "Home2";
}
function irParaUsuario() {
  paginaAtual.value = "Usuario";
}
function irParaBusca() {
  paginaAtual.value = "Busca";
}
function irParaHabilidadesNecessarias() {
  paginaAtual.value = "HabilidadesNecessarias";
}
</script>

<template>
  <main>
    <header>
<header>
  <ul>
    <li><a href="">Vagas</a></li>
    <li><a href="">Empresas</a></li>
    <li v-if="['home', 'login', 'LoginFormado', 'LoginEmpresa', 'criarEmpresas' , 'criarFormado' ,].includes(paginaAtual)">
      <button @click="irParaLogin">Login</button>
    </li>
    <li v-else>
      <img src="../public/imagens/flame.png" alt="flame.png">
    </li>
  </ul>
  <div 
    v-if="!['home', 'login', 'LoginFormado', 'LoginEmpresa', 'criarEmpresas' , 'criarFormado'].includes(paginaAtual)"
  >
    <input type="text" placeholder="Buscar..." />
    <button>
      <i class="fa-solid fa-magnifying-glass"></i>
      <img src="../public/imagens/flame6.png" alt="flame6.png">
    </button>
  </div>
</header>

    </header>
    <div v-if="paginaAtual === 'home'">
    <section>
      <p>
        Oi, somos o projeto IMT, um site com o proposito de apoiar ao egressados na sua procura no ambito laboral e
        empresas na busqueda de trabalhadores de qualidade, se tua empresa está procurando vacantes ou voce é um
        egressado que comecou no mundo do trabalho, faça o login e os ajudaremos na sua procura.
      </p>
      <p>
        Voce é:
      </p>
      <button @click="irParaCriarEmpresas">
          Empresa
      </button>
      <p>
        Ou
      </p>
      <button @click="irParaCriarFormado">
      Formado
      </button>
    </section>
    <section>
      <ul>
        <li>
          <p>
            Nossas estadisticas tem um avanço do 90%
          </p>
        </li>
        <li>
          <p>
            O 89% dos nossos graduados recebem propostas de trabalho cada semana
          </p>
        </li>
        <li>
          <p>
            O 94% das nossas empresas amigas se sentem satisfeitas com nossos graduados
          </p>
        </li>
      </ul>
    </section>
    <section>
      <p>
        No nosso site, a segurança dos seus dados pessoais é nossa prioridade. Utilizamos tecnologia de ponta para
        proteger suas informações contra acessos não autorizados. Cada passo é cuidadosamente monitorado, garantindo que
        sua privacidade seja sempre respeitada. Confie em nós para proporcionar uma experiência online segura e
        tranquila. Aqui, seu bem-estar digital é o nosso compromisso!
      </p>
    </section>
    <section>
      <p>
        Conectar-se com pessoas que podem ajudar é vital no ambiente laboral. Cada relacionamento é uma oportunidade de
        aprendizado e crescimento. Ao cultivar redes, você não só expande seu conhecimento, mas também encontra apoio e
        inspiração para alcançar seus objetivos profissionais.
      </p>
      <img src="../public/imagens/image 5(1).png" alt="image 5.png">
      <p>
        Para alcançar o sucesso profissional, é essencial adquirir habilidades específicas por meio de educação contínua
        e capacitação. Dominar conhecimentos técnicos e desenvolver competências interpessoais são passos fundamentais
        para conquistar um posto de destaque no mercado de trabalho.
      </p>
      <img src="../public/imagens/image 6(1).png" alt="image 6.png">
    </section>
  </div>
  <section v-if="paginaAtual === 'login'" id="loginFormadoSection">

    <h1>Voce é?</h1>
    <button @click="irParaLoginFormado">
      Formado
    </button>
    <button @click="irParaLoginEmpresa">
      Empresa
    </button>
  </section>
  <section>

  </section>
<section v-if="paginaAtual === 'criarEmpresas'" id="criarEmpresasSection">
  <h1>Cria sua empresa</h1>
<div>
  <ul>
    <li>
      <div>
      <input type="text" placeholder="nome da empresa">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="email">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="senha">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
  </ul>
  </div>
  <div>
  <ul>
    <li>
      <div>
      <input type="text" placeholder="Endereço">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="CNPJ">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="Confirmação da senha">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
  </ul>
</div>
  <button @click="irParaHome">
Cadastrar
  </button>
</section>
<section v-if="paginaAtual === 'criarFormado'" id="criarFormadoSection">
<h1>Cria sua conta de formado</h1>
<ul>
    <li>
      <div>
      <input type="text" placeholder="nome da empresa">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="email">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="senha">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="Confirmação da senha">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
  </ul>
  <button @click="irParaHome">
Cadastrar
  </button>
</section>
<section v-if="paginaAtual === 'LoginFormado'" id="LoginFormadoSection">
  <img src="../public/imagens/flame.png" alt="flame.png">
  <ul>
    <li>
      <div>
      <input type="text" placeholder="email">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="senha">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
  </ul>
  <button @click="irParaHome">
    login
  </button>
</section>
<section v-if="paginaAtual === 'LoginEmpresa'" id="LoginEmpresasSection">
  <img src="../public/imagens/flame.png" alt="flame.png">  
  <ul>
    <li>
      <div>
      <input type="text" placeholder="CNPJ">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
    <li>
      <div>
      <input type="text" placeholder="senha">
      <i class="fa-solid fa-magnifying-glass"></i>
    </div>
    </li>
  </ul>
  <button @click="irParaHome">
    login
  </button>
</section>
<section v-if="paginaAtual === 'Home2'" id="homeSection">
  <div>
    <button>
    <input type="text" placeholder="Criar uma publicação">
    <i class="fa-solid fa-magnifying-glass"></i>
    <img src="../public/imagens/flame5.png" alt="flame5.png">
  </button>
  <img src="../public/imagens/flame2.png" alt="flame2.png">
  <h2>
    Empresa tal
  </h2>
  <p>
    Numa cidade onde as noites eram mais claras que os dias, havia um pequeno café chamado Estelar. Ficava na esquina de uma rua que não aparecia nos mapas, mas todo mundo que precisava de um pouco de paz acabava encontrando o lugar.
  </p>
  <ul>
    <li>
      <p>
        Horarios
      </p>
    </li>
    <li>
      Salario
    </li>
    <li>
      Lugar
    </li>
    <li>
      Demais informações
    </li>
  </ul>
  <img src="../public/imagens/flame2.png" alt="flame2.png">
  <h2>
    Empresa sla
  </h2>
  <p>
    Lá dentro, o tempo parecia andar devagar. As paredes estavam cobertas de livros esquecidos, e cada mesa tinha uma vela que só acendia quando alguém sentava com o coração aberto
  </p>
  <ul>
    <li>
      <p>
        Horarios
      </p>
    </li>
    <li>
      Salario
    </li>
    <li>
      Lugar
    </li>
    <li>
      Demais informações
    </li>
  </ul>
  </div>
  <div>
<ul>
  <li>
    <img src="../public/imagens/flame.png" alt="flame.png">
    <p>
      Nome: ******
      Especialização: ******
      Localidade: ******
      Local de Estudos: *******
    </p>
  </li>
  <li>
    <p>Notificações</p>
    <img src="../public/imagens/flame4.png" alt="flame4.png">
  </li>
  <li>
    <img src="../public/imagens/flame3.png" alt="flame3.png">
    <p>
      Curriculum
    </p>
  </li>
</ul>
  </div>
</section>
  </main>
  <footer>
    <img src="../public/imagens/Captura de tela de 2025-07-04 13-40-50-Photoroom 1.png"
      alt="Captura de tela de 2025-07-04 13-40-50-Photoroom.png">
    <ul>
      <li>
        <p>
          <a href="">Geral</a>
        </p>
      </li>
      <li>
        <button @click="irParaLogin">
        login
        </button>
      </li>
      <li>
        <p>
          <a href="">Empresas</a>
        </p>
      </li>
      <li>
        <p>
          <a href="">Vagas</a>
        </p>
      </li>
    </ul>
    <ul>
      <li>
        <a href="https://x.com/IMT184516329585"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M389.2 48h70.6L305.6 224.2 487 464H345L233.7 318.6 106.5 464H35.8L200.7 275.5 26.8 48H172.4L272.9 180.9 389.2 48zM364.4 421.8h39.1L151.1 88h-42L364.4 421.8z"/></svg></a>
        
      </li>
      <li>
        <a href="https://www.facebook.com/profile.php?id=61579092402663"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M512 256C512 114.6 397.4 0 256 0S0 114.6 0 256C0 376 82.7 476.8 194.2 504.5V334.2H141.4V256h52.8V222.3c0-87.1 39.4-127.5 125-127.5c16.2 0 44.2 3.2 55.7 6.4V172c-6-.6-16.5-1-29.6-1c-42 0-58.2 15.9-58.2 57.2V256h83.6l-14.4 78.2H287V510.1C413.8 494.8 512 386.9 512 256h0z"/></svg></a>
      </li>
      <li>
        <a href="https://www.instagram.com/imt_hackaton/"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.<path d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"/></svg></a>
      </li>
    </ul>
    <p>&copy;2025 Copyright</p>
  </footer>
</template>

<style scoped>

</style>