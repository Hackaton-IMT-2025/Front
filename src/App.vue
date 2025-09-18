<script setup>
import { ref } from 'vue'
const paginaAtual = ref('home')

function irParaLogin() {
  paginaAtual.value = 'login'
}
function irParaCriarEmpresas() {
  paginaAtual.value = 'criarEmpresas'
}
function irParaCriarFormado() {
  paginaAtual.value = 'criarFormado'
}
function irParaLoginFormado() {
  paginaAtual.value = 'LoginFormado'
}
function irParaLoginEmpresa() {
  paginaAtual.value = 'LoginEmpresa'
}
function irParaHome() {
  paginaAtual.value = 'Home'
}
function irParaBusca() {
  paginaAtual.value = 'irParaBusca'
}
function irParaHabilidadesNecessarias() {
  paginaAtual.value = 'irParaHabilidadesNecessarias'
}
function irParaUsuario() {
  paginaAtual.value = 'irParaUsuario'
}
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

window.addEventListener("load", () => {
  gsap.to(".lado-esquerdo", {
    opacity: 0.3, // diminui a visibilidade do gradiente
    scrollTrigger: {
      trigger: ".background",
      start: "top top",
      end: "bottom bottom",
      scrub: true,
    },
  });

  gsap.to(".lado-direito", {
    opacity: 0.3,
    scrollTrigger: {
      trigger: ".background",
      start: "top top",
      end: "bottom bottom",
      scrub: true,
    },
  });
});


window.addEventListener("load", () => {
  gsap.to(".lado-esquerdo2", {
    opacity: 0.3, // diminui a visibilidade do gradiente
    scrollTrigger: {
      trigger: ".background2",
      start: "top top",
      end: "bottom bottom",
      scrub: true,
    },
  });

  gsap.to(".lado-direito2", {
    opacity: 0.3,
    scrollTrigger: {
      trigger: ".background2",
      start: "top top",
      end: "bottom bottom",
      scrub: true,
    },
  });
});


window.addEventListener("load", () => {
  gsap.to(".lado-esquerdo3", {
    opacity: 0.3, // diminui a visibilidade do gradiente
    scrollTrigger: {
      trigger: ".background3",
      start: "top top",
      end: "bottom bottom",
      scrub: true,
    },
  });

  gsap.to(".lado-direito3", {
    opacity: 0.3,
    scrollTrigger: {
      trigger: ".background3",
      start: "top top",
      end: "bottom bottom",
      scrub: true,
    },
  });
});






</script>
<template>
  
  <main class="mainpage">
    <header>
      <nav v-if="
        [
          'home',
          'login',
          'LoginFormado',
          'LoginEmpresa',
          'criarEmpresas',
          'criarFormado',
        ].includes(paginaAtual)
      ">
        <div><img src="../public/imagens/Logo-Photoroom 1.png" alt="Logo IMT" /></div>
        <ul>
          <li><a href="#">Vagas</a></li>
          <li><a href="#">Empresas</a></li>
          <li>
            <button @click="irParaLogin">Login</button>
          </li>
        </ul>
      </nav>
      <nav v-else>
        <div>
          <div>
            <img  @click="irParaHome" class="logo2" src="../public/imagens/Logo-Photoroom 1.png" alt="Logo IMT" />
          </div>
          <div class="search-wrapper">
            <input type="text" placeholder="Buscar" />
            <img class="lupa" @click="irParaBusca" src="../public/imagens/flame6.png" alt="flame6.png">
          </div>
        </div>
        <ul>
          <li><a href="#">Inicio</a></li>
          <li><a @click="irParaBusca" href="#">Vagas</a></li>
          <li><a @click="irParaBusca" href="#">Empresas</a></li>
          <li>
            <img @click="irParaUsuario" class="avatar" src="../public/imagens/flame.png" alt="Avatar" />
          </li>
        </ul>
      </nav>
    </header>
    <div v-if="paginaAtual === 'home'">
      <div class="background">
        <div class="degrade-top"></div>
        <div class="lado-esquerdo"></div>
        <div class="lado-direito"></div>
        <section class="hero">
          <p class="oi">
            Oi, somos o projeto IMT, um site com o proposito de apoiar ao egressados na sua procura
            no ambito laboral e empresas na busqueda de trabalhadores de qualidade, se tua empresa
            está procurando vacantes ou voce é um egressado que comecou no mundo do trabalho, faça o
            login e os ajudaremos na sua procura.
          </p>
          <p>Voce é:</p>
          <div class="escolha">
            <button @click="irParaCriarEmpresas">Empresa</button>
            <p>Ou</p>
            <button @click="irParaCriarFormado">Formado</button>
          </div>
          <h1 class="imt">INTRODUÇÃO AO MUNDO DO TRABALHO</h1>
        </section>
        <div class="degrade-bottom2"></div>
      </div>
      <div class="background2">
        <div class="degrade-top2"></div>
        <div class="lado-esquerdo2"></div>
        <div class="lado-direito2"></div>
        <section class="nonosso">
          <p class="pnonosso">
            No nosso site, a segurança dos seus dados pessoais é nossa prioridade. Utilizamos
            tecnologia de ponta para proteger suas informações contra acessos não autorizados. Cada
            passo é cuidadosamente monitorado, garantindo que sua privacidade seja sempre
            respeitada. Confie em nós para proporcionar uma experiência online segura e tranquila.
            Aqui, seu bem-estar digital é o nosso compromisso!
          </p>
          <ul>
            <li>
              <p>Nossas estadisticas tem um avanço do 90%</p>
            </li>
            <li>
              <p>O 89% dos nossos graduados recebem propostas de trabalho cada semana</p>
            </li>
            <li>
              <p>O 94% das nossas empresas amigas se sentem satisfeitas com nossos graduados</p>
            </li>
          </ul>
        </section>
        <div class="degrade-bottom2"></div>
      </div>
      <div class="background3">
        <div class="degrade-top3"></div>
        <div class="lado-esquerdo3"></div>
        <div class="lado-direito3"></div>
        <section class="conectar">
          <div class="cima">
            <p>
              Conectar-se com pessoas que podem ajudar é vital no ambiente laboral. Cada
              relacionamento é uma oportunidade de aprendizado e crescimento. Ao cultivar redes,
              você não só expande seu conhecimento, mas também encontra apoio e inspiração para
              alcançar seus objetivos profissionais.
            </p>
            <img src="../public/imagens/image 5(1).png" alt="image 5.png" />
          </div>
          <div class="baixo">
            <img src="../public/imagens/image 6(1).png" alt="image 6.png" />
            <p>
              Para alcançar o sucesso profissional, é essencial adquirir habilidades específicas por
              meio de educação contínua e capacitação. Dominar conhecimentos técnicos e desenvolver
              competências interpessoais são passos fundamentais para conquistar um posto de
              destaque no mercado de trabalho.
            </p>
          </div>
        </section>
        <div class="degrade-bottom3"></div>
      </div>
    </div>
    <transition name="fade">
      <div class="background" v-if="paginaAtual === 'login'">
        <div class="degrade-top"></div>
        <div class="lado-esquerdo"></div>
        <div class="lado-direito"></div>

        <section class="vocee" id="loginFormadoSection">
          <h1>Você é?</h1>
          <button @click="irParaLoginFormado">Formado</button>
          <button @click="irParaLoginEmpresa">Empresa</button>
        </section>

        <div class="degrade-bottom"></div>
      </div>
    </transition>
    <transition name="fade">
      <div class="background" v-if="paginaAtual === 'criarEmpresas'">
        <div class="degrade-top"></div>
        <div class="lado-esquerdo"></div>
        <div class="lado-direito"></div>

        <section class="criarempresa" id="criarEmpresasSection">
          <h1>Criar sua empresa</h1>
          <div class="todo">
            <div>
              <ul>
                <li>
                  <div>
                    <input type="text" placeholder="nome da empresa" />
                    <i class="fa-solid fa-magnifying-glass"></i>
                  </div>
                </li>
                <li>
                  <div>
                    <input type="text" placeholder="email" />
                    <i class="fa-solid fa-magnifying-glass"></i>
                  </div>
                </li>
                <li>
                  <div>
                    <input type="text" placeholder="senha" />
                    <i class="fa-solid fa-magnifying-glass"></i>
                  </div>
                </li>
              </ul>
            </div>

            <div>
              <ul>
                <li>
                  <div>
                    <input type="text" placeholder="Endereço" />
                    <i class="fa-solid fa-magnifying-glass"></i>
                  </div>
                </li>
                <li>
                  <div>
                    <input type="text" placeholder="CNPJ" />
                    <i class="fa-solid fa-magnifying-glass"></i>
                  </div>
                </li>
                <li>
                  <div>
                    <input type="text" placeholder="Confirmação da senha" />
                    <i class="fa-solid fa-magnifying-glass"></i>
                  </div>
                </li>
              </ul>
            </div>
          </div>

          <button @click="irParaHome">Cadastrar</button>
        </section>

        <div class="degrade-bottom"></div>
      </div>
    </transition>
    <transition name="fade">
      <div class="background" v-if="paginaAtual === 'criarFormado'">
        <div class="degrade-top"></div>
        <div class="lado-esquerdo"></div>
        <div class="lado-direito"></div>
        <section class="criarformado" v-if="paginaAtual === 'criarFormado'" id="criarFormadoSection">
          <h1>Criar sua conta de formado</h1>
          <ul>
            <li>
              <div>
                <input type="text" placeholder="nome do formado" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
            <li>
              <div>
                <input type="text" placeholder="email" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
            <li>
              <div>
                <input type="text" placeholder="senha" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
            <li>
              <div>
                <input type="text" placeholder="Confirmação da senha" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
          </ul>
          <button @click="irParaHome">Cadastrar</button>
        </section>
        <div class="degrade-bottom"></div>
      </div>
    </transition>
    <transition name="fade">
      <div class="background" v-if="paginaAtual === 'LoginFormado'">
        <div class="degrade-top"></div>
        <div class="lado-esquerdo"></div>
        <div class="lado-direito"></div>
        <section class="loginformado" v-if="paginaAtual === 'LoginFormado'" id="LoginFormadoSection">
          <img src="../public/imagens/flame.png" alt="flame.png" />
          <ul>
            <li>
              <div>
                <input type="text" placeholder="email" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
            <li>
              <div>
                <input type="text" placeholder="senha" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
          </ul>
          <button @click="irParaHome">login</button>
        </section>
        <div class="degrade-bottom"></div>
      </div>
    </transition>
    <transition name="fade">
      <div class="background" v-if="paginaAtual === 'LoginEmpresa'">
        <div class="degrade-top"></div>
        <div class="lado-esquerdo"></div>
        <div class="lado-direito"></div>
        <section class="loginempresa" v-if="paginaAtual === 'LoginEmpresa'" id="LoginEmpresasSection">
          <img src="../public/imagens/flame.png" alt="flame.png" />
          <ul>
            <li>
              <div>
                <input type="text" placeholder="CNPJ" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
            <li>
              <div>
                <input type="text" placeholder="senha" />
                <i class="fa-solid fa-magnifying-glass"></i>
              </div>
            </li>
          </ul>
          <button @click="irParaHome">login</button>
        </section>
        <div class="degrade-bottom"></div>
      </div>
    </transition>
    <div class="background2" v-if="paginaAtual === 'Home'">
      <div class="degrade-top2"></div>
      <div class="lado-esquerdo2"></div>
      <div class="lado-direito2"></div>
      <section class="home" v-if="paginaAtual === 'Home'" id="HomeSection">
        <div>
        <div class="criarpublicacao">
          <input type="text" placeholder="Criar uma publicação" />
          <i class="fa-solid fa-magnifying-glass"></i>
          <img src="../public/imagens/flame5.png" alt="flame5.png" />
        </div>
        <div>
        <div  class="p">
          <img class="pi" src="../public/imagens/flame2.png" alt="flame2.png" />
          <div>
              <h2>Empresa tal</h2>
              <p>
                Numa cidade onde as noites eram mais claras que os dias, havia um pequeno café
                chamado Estelar. Ficava na esquina de uma rua que não aparecia nos mapas, mas todo
                mundo que precisava de um pouco de paz acabava encontrando o lugar.
              </p>
            <ul>
            <li class="demais">
              <p>Horarios</p>
            </li>
            <li class="demais">
              <p>Salario</p>
            </li>
            <li class="demais">
              <p>Localização</p>
            </li>
            <li class="demais">
              <p>Demais informações</p>
            </li>
          </ul>
          </div>
          </div>
          <div class="p">
             <img class="pi" src="../public/imagens/flame2.png" alt="flame2.png" />
              <div>
              <h2>Empresa tal</h2>
              <p>
                Numa cidade onde as noites eram mais claras que os dias, havia um pequeno café
                chamado Estelar. Ficava na esquina de uma rua que não aparecia nos mapas, mas todo
                mundo que precisava de um pouco de paz acabava encontrando o lugar.
              </p>
              <ul>
            <li class="demais">
              <p>Horarios</p>
            </li>
            <li class="demais">
              <p>Salario</p>
            </li>
            <li class="demais">
              <p>Localização</p>
            </li>
            <li class="demais">
              <p>Demais informações</p>
            </li>
          </ul>
          </div>
        </div>
        </div>
        </div>
        <div>
        <div class="curriculo">
            <div class="nell">
              <img src="../public/imagens/flame.png" alt="flame.png" />
              <p>
                  Nome: ****** <br>
                  Especialização: ****** <br>
                  Localidade: ******<br>
                  Local de Estudos: *******<br>
              </p>
              </div>
              <div class="lembretes">
              <p>Notificações</p>
              <img  class="curriculum" src="../public/imagens/flame4.png" alt="flame4.png" />
              </div>
              <div class="lembretes">
                <p>Curriculum</p>
              <img class="curriculum2" src="../public/imagens/flame3.png" alt="flame3.png" />
              </div>
        </div>
        </div>
      </section>
      <div class="degrade-bottom2"></div>
    </div>
      <div class="background2" v-if="paginaAtual === 'irParaBusca'">
        <div class="degrade-top2"></div>
        <div class="lado-esquerdo2"></div>
        <div class="lado-direito2"></div>
    <section class="buscas" v-if="paginaAtual === 'irParaBusca'" id="irParaBuscaSection">
      <div>
        <div class="branco">
        <ul>
          <li>
            <img src="../public/imagens/flame2.png" alt="flame2.png" />
          </li>
          <li>
            <h2>Empresa Salario</h2>
            <p>Precisamos estagiario de desenvolvedor em java</p>
          </li>
        </ul>
        </div>
        <div class="branco">
        <ul>
          <li>
            <img src="../public/imagens/flame2.png" alt="flame2.png" />
          </li>
          <li>
            <h2>Empresa Salario</h2>
            <p>Precisamos estagiario de desenvolvedor em java</p>
          </li>
        </ul>
        </div>
        <div class="branco">
        <ul>
          <li>
            <img src="../public/imagens/flame2.png" alt="flame2.png" />
          </li>
          <li>
            <h2>Empresa Salario</h2>
            <p>Precisamos estagiario de desenvolvedor em java</p>
          </li>
        </ul>
        </div>
        <div class="branco">
        <ul>
          <li>
            <img src="../public/imagens/flame2.png" alt="flame2.png" />
          </li>
          <li>
            <h2>Empresa Salario</h2>
            <p>Precisamos estagiario de desenvolvedor em java</p>
          </li>
        </ul>
        </div>
      </div>
      <div>
        <div class="branco2">
        <ul class="es">
          <li class="esbranco">
            <img src="../public/imagens/flame2.png" alt="flame2.png" />
            <h2>Empresa Salario</h2>
          </li>
          <li>
            <p>
              Lá dentro, o tempo parecia andar devagar. As paredes estavam cobertas de livros
              esquecidos, e cada mesa tinha uma vela que só acendia quando alguém sentava com o
              coração aberto
            </p>
          </li>
          <li>
            <button @click="irParaHabilidadesNecessarias">Habilidades necessarias</button>
          </li>
          <li>
            <p class="hsml">
              Horário:**************** <br>
               Salario:********* <br>
                Modalidade:**************** <br>
              Localização:****************** <br>
            </p>
          </li>
          <li>
            <p>
              Lá dentro, o tempo parecia andar devagar. As paredes estavam cobertas de livros
              esquecidos, e cada mesa tinha uma vela que só acendia quando alguém sentava com o
              coração aberto
            </p>
          </li>
          <li>
            <button class="candidatar">Candidatar-se</button>
          </li>
          <li>
            <button class="ec">Enviar curriculum</button>
          </li>
        </ul>
        </div>
      </div>
    </section>
    <div class="degrade-bottom2"></div>
    </div>

        <div class="background2" v-if="paginaAtual === 'irParaHabilidadesNecessarias'">
        <div class="degrade-top2"></div>
        <div class="lado-esquerdo2"></div>
        <div class="lado-direito2"></div>
    <section class="habilidades" v-if="paginaAtual === 'irParaHabilidadesNecessarias'" id="irParaHabilidadesNecessariasSection">
<div>
  <div class="branco">
      <ul>
        <li>
<h2 class="hqv">Habilidades que voce possui e são requeridas para o cargo</h2>
<img src="../public/imagens/flame1.png" alt="flame1.png" />
        </li>
        <li>
          <button class="hb">Habilidades</button>
        </li>
        <li>
          <button class="hb">Habilidades</button>
        </li>
        <li>
          <button class="hb">Habilidades</button>
        </li>
        <li>
          <h2>Habilidades que voce não possui e são requeridas para o cargo</h2>
        </li>
        <li>
          <button><p>Habilidades</p> <img src="../public/imagens/flame5.png" alt="flame5.png" /></button>
        </li>
        <li>
          <button><p>Habilidades</p> <img src="../public/imagens/flame5.png" alt="flame5.png" /></button>
        </li>
        <li>
          <button><p>Habilidades</p> <img src="../public/imagens/flame5.png" alt="flame5.png" /></button>
        </li>
        <li>
          <button><p>Habilidades</p> <img src="../public/imagens/flame5.png" alt="flame5.png" /></button>
        </li>
      </ul>
      </div>
      </div>
    </section>
    <div class="degrade-bottom2"></div>
    </div>


    <section v-if="paginaAtual === 'irParaUsuario'" id="irParaUsuarioSection">
      <div class="background2" v-if="paginaAtual === 'irParaUsuario'">
        <div class="degrade-top2"></div>
        <div class="lado-esquerdo2"></div>
        <div class="lado-direito2"></div>
      <section class="usuario">
      <button class="agregar">
       <p> Agregar habilidades</p> <img src="../public/imagens/flame5.png" alt="flame5.png" />
      </button>
      <div class="ana">
        <h2>Voce possui alguma condição física ou mental?</h2>
        <p>Se sim, por favor anexe o documento comprovante</p>
        <button>Documento Anexado</button>
        <div class="vs">
          <button>Anexar</button>
          <button>Não possuo</button>
          <button>Atualizar</button>
        </div>
      </div>
       <div class="ana">
        <h2>Voce possui algum certificado ou diploma?</h2>
        <p>
          Se sim, por favor anexe o documento comprovante, deve possuir codigo QR e conter suas
          informações pessoais e da instituição na qual se formou, além da carga horária.
        </p>
        <button>documento Anexado</button>
        <div class="vs">
          <button>Anexar</button>
          <button>Não possuo</button>
          <button>Atualizar</button>
        </div>
      </div>
      </section>
      <div class="degrade-bottom2"></div>
    </div>
    <div class="background2" v-if="paginaAtual === 'irParaUsuario'">
        <div class="degrade-top2"></div>
        <div class="lado-esquerdo2"></div>
        <div class="lado-direito2"></div>
      <section class="usuario">
          <button class="localidade">
     <p> Localidade</p> <img src="../public/imagens/flame5.png" alt="flame5.png" />
     </button>
      <div class="ana">
      <div>
        <h2>Qual seria seu lugar de trabalho?</h2>
        <div class="vs">
          <button>Empresa</button>
          <button>Remoto</button>
          <button>Integral</button>
        </div>
        </div>
      </div>
      <div class="ana">
        <h2>Voce possui algum certificado ou diploma?</h2>
        <p>
          Se sim, por favor anexe o documento comprovante, deve possuir codigo QR e conter suas
          informações pessoais e da instituição na qual se formou, além da carga horária.
        </p>
        <div class="vs">
          <button>Anexar</button>
          <button>Não possuo</button>
          <button>Atualizar</button>
        </div>
        </div>
      </section>
      <div class="degrade-bottom2"></div>
    </div>
    </section>

    <section v-if="paginaAtual === 'irParaSelecaodecandidatos'" id="irParaSelecaodecandidatosSection">
      <ul>
        <li>
          <img src="../public/imagens/flame2.png" alt="flame2.png" />
          <h1>Nome</h1>
          <button>Mostrar informações</button>
        </li>
        <li>
          <img src="../public/imagens/flame7.png" alt="flame7.png" />
          <h1>Nome</h1>
          <button>Mostrar informações</button>
        </li>
        <li>
          <img src="../public/imagens/flame2.png" alt="flame2.png" />
          <h1>Nome</h1>
          <button>Mostrar informações</button>
        </li>
        <li>
          <img src="../public/imagens/flame7.png" alt="flame7.png" />
          <h1>Nome</h1>
          <button>Mostrar informações</button>
        </li>
        <li>
          <img src="../public/imagens/flame2.png" alt="flame2.png" />
          <h1>Nome</h1>
          <button>Mostrar informações</button>
        </li>
        <li>
          <img src="../public/imagens/flame2.png" alt="flame2.png" />
          <h1>Nome</h1>
          <button>Mostrar informações</button>
        </li>
      </ul>
      <button>
        Enviar solicitudes aprovadas <img src="../public/imagens/flame9.png" alt="flame9.png" />
      </button>
      <button>
        Eliminar solicitudes <img src="../public/imagens/flame8.png" alt="flame8.png" />
      </button>
    </section>
    <section v-if="paginaAtual === 'irParaComunicacaocomcandidatos'" id="irParaComunicacaocomcandidatosSection">
      <div>
        <ul>
          <li>
            <img src="../public/imagens/flame7.png" alt="flame7.png" />
            <h1>Nome</h1>
            <p>Descrição do cara</p>
            <img src="../public/imagens/flame10.png" alt="flame10.png" />
          </li>
          <li>
            <img src="../public/imagens/flame7.png" alt="flame7.png" />
            <h1>Nome</h1>
            <p>Descrição do cara</p>
            <img src="../public/imagens/flame10.png" alt="flame10.png" />
          </li>
          <li>
            <img src="../public/imagens/flame7.png" alt="flame7.png" />
            <h1>Nome</h1>
            <p>Descrição do cara</p>
            <img src="../public/imagens/flame10.png" alt="flame10.png" />
          </li>
        </ul>
      </div>
      <div>
        <h1>Aos candidatos seleccionados voce pode enviar o seguinte mensagem:</h1>
        <p>
          Voce terá uma entrevista conosco! Esperamos voce na data ******* as ***** horas
          Localização: ********************* Por favor trouza sua documentação impressa com você
        </p>
        <p>
          Você foi para segunda etapa! A segunda etapa foi começada, agora voce terá que esperar
          enquanto nossa equipe avalia sua informação e documentos, entraremos em contacto com você.
        </p>
        <p>Mensagem personalizada</p>
      </div>
    </section>
    <section v-if="paginaAtual === 'irParaComunicacaocomempresas'" id="irParaComunicacaocomempresasSection">
      <div>
        <ul>
          <li>
            <img src="../public/imagens/flame7.png" alt="flame7.png" />
            <h1>Nome</h1>
            <p>Descrição da empresa</p>
            <img src="../public/imagens/flame10.png" alt="flame10.png" />
          </li>
          <li>
            <img src="../public/imagens/flame7.png" alt="flame7.png" />
            <h1>Nome</h1>
            <p>Descrição da empresa</p>
            <img src="../public/imagens/flame10.png" alt="flame10.png" />
          </li>
          <li>
            <img src="../public/imagens/flame7.png" alt="flame7.png" />
            <h1>Nome</h1>
            <p>Descrição da empresa</p>
            <img src="../public/imagens/flame10.png" alt="flame10.png" />
          </li>
        </ul>
      </div>
      <div>
        <h1>Voce pode mandar mensagens a(as) empresas seleccionados:</h1>
        <p>
          Confirmo minha presença na empresa ********** na data ********, as **** horas, para a
          entrevista presencial Atentamente ************
        </p>
        <p>
          Mando o comunicado informando que não vou comparecer na entrevista, obrigada pela
          oportunidade e sorte na procura de funcionarios. Atentamente ************
        </p>
        <p>Mensagem personalizada</p>
      </div>
    </section>
  </main>
  <footer>

    <ul>
      <div>
      <li>
        <a href="https://x.com/IMT184516329585"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
            Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
            https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
            <path
              d="M389.2 48h70.6L305.6 224.2 487 464H345L233.7 318.6 106.5 464H35.8L200.7 275.5 26.8 48H172.4L272.9 180.9 389.2 48zM364.4 421.8h39.1L151.1 88h-42L364.4 421.8z" />
          </svg></a>
      </li>
      <li>
        <a href="https://www.facebook.com/profile.php?id=61579092402663"><svg xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512">
            Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
            https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
            <path
              d="M512 256C512 114.6 397.4 0 256 0S0 114.6 0 256C0 376 82.7 476.8 194.2 504.5V334.2H141.4V256h52.8V222.3c0-87.1 39.4-127.5 125-127.5c16.2 0 44.2 3.2 55.7 6.4V172c-6-.6-16.5-1-29.6-1c-42 0-58.2 15.9-58.2 57.2V256h83.6l-14.4 78.2H287V510.1C413.8 494.8 512 386.9 512 256h0z" />
          </svg></a>
      </li>
      <li>
        <a href="https://www.instagram.com/imt_hackaton/"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License -
            https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.
            <path
              d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z" />
          </svg></a>
      </li>
      </div>
      <p class="copy">&copy;2025 Copyright</p>
    </ul>

    <ul class="geral">
      <li>
        <p>
          <a href="">Geral</a>
        </p>
      </li>
      <li>
        <button cla @click="irParaLogin">Login</button>
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
<img src="../public/imagens/Logo-Photoroom 1.png" alt="Logo-Photoroom 1.png" />
  </footer>
</template>
<style scoped>
/*==============================================
                  background
===============================================*/
.background {
  background: #08081e;
  display: flex;
  height: 120vh;
  position: relative;
  align-items: center;
}

.degrade-top,
.degrade-bottom {
  position: absolute;
  left: 0;
  width: 100%;
  height: 150px;
  z-index: 5;
  pointer-events: none;
}

.degrade-top {
  top: 0;
  background: linear-gradient(to bottom, #0d0d36, rgba(8, 8, 30, 0));
  z-index: 1;
}

.degrade-bottom {
  bottom: 0;
  background: linear-gradient(to top, #0d0d36, rgba(8, 8, 30, 0));
}

.lado-esquerdo {
  width: 50%;
  background: conic-gradient(from 90deg at 50% 75%, #0c0c0c 0deg, #b1b1b1 200deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
}

.lado-direito {
  width: 52%;
  background: conic-gradient(from 90deg at 50% 75.01%, #0c0c0c 0deg, #b1b1b1 200deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
  transform: scaleX(-1);
}


/*==============================================
                  background2
===============================================*/
.background2 {
  background: #08081e;
  display: flex;
  height: 130vh;
  width: 100%;
  position: relative;
}

.degrade-top2,
.degrade-bottom2 {
  position: absolute;
  left: 0;
  width: 100%;
  height: 150px;
  z-index: 5;
  pointer-events: none;
}

.degrade-top2 {
  top: 0;
  background: linear-gradient(to bottom, #0d0d36, rgba(8, 8, 30, 0));
  z-index: 1;
}

.degrade-bottom2 {
  bottom: 0;
  background: linear-gradient(to top, #0d0d36, rgba(8, 8, 30, 0));
}

.lado-esquerdo2 {
  width: 50%;
  background: conic-gradient(from 90deg at 50% 75%, #f8f8f8 0deg , #0c0c0c 6deg, #b1b1b1 355deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
}

.lado-direito2 {
  width: 52%;
  background: conic-gradient(from 90deg at 50% 75.01%, #f8f8f8 0deg , #0c0c0c 6deg, #b1b1b1 355deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
  transform: scaleX(-1);
}

/*==============================================
                  background3
===============================================*/
.background3 {
  background: #08081e;
  display: flex;
  height: 100vh;
  width: 100%;
  position: relative;
}

.degrade-top3,
.degrade-bottom3 {
  position: absolute;
  left: 0;
  width: 100%;
  height: 150px;
  z-index: 5;
  pointer-events: none;
}

.degrade-top3 {
  top: 0;
  background: linear-gradient(to bottom, #0d0d36, rgba(8, 8, 30, 0));
  z-index: 1;
}

.degrade-bottom3 {
  bottom: 0;
  background: linear-gradient(to top, #0d0d36, rgba(8, 8, 30, 0));
}

.lado-esquerdo3 {
  width: 50%;
  background: conic-gradient(from 90deg at 50% 50%,#f8f8f8 0deg,  #0c0c0c 6deg, #b1b1b1 355deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
}

.lado-direito3 {
  width: 52%;
  background: conic-gradient(from 90deg at 50% 50.01%, #f8f8f8 0deg, #0c0c0c 6deg, #b1b1b1 355deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
  transform: scaleX(-1);
}

/*==========================
         HEADER
===========================*/
header nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 80px;
  padding: 0 40px;
  z-index: 10;
  margin: 50px 0;
}

header img {
  height: 100px;
  object-fit: contain;
  margin: 0px 0px 0px 70px;
}
.logo2{
  margin: -10px;
}

header ul {
  display: flex;
  align-items: center;
  gap: 50px;
  list-style: none;
  margin: 0px 50px 0px 0px;
  padding: 0;
}

header ul li {
  display: flex;
  align-items: center;
}

header ul li a,
header ul li p {
  text-decoration: none;
  color: #fff;
  font-weight: 500;
  font-size: 23px;
  transition: color 0.3s ease;
  font-family: poppins;
}

header ul li a:hover,
header ul li p:hover {
  color: #b1b1b1;
  cursor: pointer;
  transform: scale(1.1);
}

header ul li button {
  background: #fff;
  color: #0c0c0c;
  padding: 12px 23px;
  border: none;
  border-radius: 100px;
  cursor: pointer;
  font-weight: bold;
  transition:
    background 0.3s,
    color 0.3s;
  font-size: 18px;
  font-family: poppins;
}

header ul li button:hover {
  background: #b1b1b1;
  color: #000;
}

header div {
  display: flex;
  align-items: center;
  gap: 10px;
}

header button i {
  color: white;
  font-size: 16px;
}

header nav div div.search-wrapper input {
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 10px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  color: #f8f8f8;
  text-decoration: none;
  font-size: 18px;
}

header nav div {
  display: flex;
}header nav div div input{
padding: 18px 400px 18px 20px;
border-radius:200px ;
}header .avatar{
  height: 60px;
  object-fit: contain;
  margin: 0px 20px 0px 0px;
}header .lupa{
  height: 65px;
  position: absolute;
  margin: 10px 0px 0px 610px;
}header img:hover {
  transform: scale(1.1);
}

/*=============================
         HERO (main)
==============================*/
.hero {
  position: absolute;
  text-align: center;
  margin: 20px auto;
  width: 100%;
  justify-content: center;
}

.hero p.oi {
  line-height: 1.6;
  color: #ddd;
  max-width: 100vh;
  width: 100%;
  margin: -100px auto 30px auto;
}

.hero .imt {
  font-size: 5rem;
  color: #b1b1b1;
  font-weight: bold;
  mix-blend-mode: color-dodge;
  font-family: Annapurna SIL;
  line-height: 1.4;
  max-width: 150vh;
  margin: 10px auto;
}

/*=============================
   ESCOLHA (botões)/ geral
==============================*/
.escolha {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 40px;
  margin: 30px 0;
}

button {
  padding: 12px 28px;
  border: none;
  border-radius: 30px;
  background-color: #fff;
  color: #0d0d36;
  font-weight: bold;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  font-weight: normal;
}

button:hover {
  background-color: #d4d4d4;
  transform: scale(1.05);
}

h1 {
  font-size: 4rem;
  font-weight: bolder;
  margin: 60px 0px;
  mix-blend-mode: color-dodge;
  color: #b1b1b1;
}

ul li div input {
  padding: 12px 200px 12px 80px;
  font-size: 16px;
  border-radius: 5px;
  border-style: none;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.6s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/*=============================
            TEXTOS
==============================*/
.hero span,
.hero small {
  color: #ccc;
  font-size: 1rem;
  margin-top: 10px;
}

.hero .ou {
  margin: 0 10px;
  color: #aaa;
}

/*=============================
            NO NOSSO
==============================*/
.nonosso {
  position: absolute;
  align-items: center;
  justify-content: center;
  text-align: center;
  width: 100%;
  margin: 340px 0px;
}

.nonosso ul {
  display: flex;
  padding: 20px;
  align-items: center;
  justify-content: center;
}

.nonosso ul li {
  padding: 20px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 10px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  max-width: 250px;
  margin: 25px 20px;
  line-height: 1.6;
  text-align: center;
}

.pnonosso {
  line-height: 1.6;
  max-width: 100vh;
  margin: auto;
}

/*=============================
           CONECTAR
==============================*/
.conectar {
  width: 100%;
  height: 100%;
  display: flex;
  position: absolute;
  align-items: center;
  margin: 10px auto;
  display: grid;
  grid-template-columns: 1fr;
}
.conectar p {
  max-width: 50vh;
  min-width: 30vh;
  height: 27vh;
  margin: 0px 0px;
  line-height: 1.5;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 10px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 24px 40px;
  object-fit: cover;
  margin: 0px 20px;

}

.conectar div {
  display: flex;
  align-items: center;
  justify-content: center;
}

.conectar div img {
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 10px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 10px;
  object-fit: cover;
  width: 50vh;
  height: 30vh;
}

/*=================================
              VOCE É
=================================*/
.vocee {
  position: absolute;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 190px 0px;
  width: 100%;
  height: 100%;
}

.vocee h1 {
  font-size: 4rem;
  font-weight: bolder;
  margin: 60px 0px;
  mix-blend-mode: color-dodge;
  color: #b1b1b1;
  margin: 260px 0px 80px 0px ;
}

.vocee button {
  margin: 0px 40px;
  padding: 18px 20px;
  font-size: 20px;
  font-weight: normal;
}

/*=================================
          criar sua empresa
=================================*/
.criarempresa {
  position: absolute;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 190px 0px;
  width: 100%;
  height: 100%;
}

.todo {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px;
}

.criarempresa h1 {
  font-size: 3rem;
  margin: 330px 0px 60px 0px;
}

.criarempresa ul li {
  margin: 30px;
}

.criarempresa button {
  margin: 60px 0px;
  font-size: 1.5rem;
  font-weight: normal;
}

/*=================================
        criar conta de formado
=================================*/
.criarformado {
  position: absolute;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 150px 0px;
  width: 100%;
  height: 100%;
}

.criarformado ul li {
  margin: 30px;
}

.criarformado ul li div input {
  padding: 12px 200px 12px 20px;
}

.criarformado button {
  margin: 60px 0px;
  font-size: 1.5rem;
  font-weight: normal;
}

.criarformado h1 {
  font-size: 3rem;
  margin: 290px 0px 70px 0px;
}

/*=================================
        login formado/empresa
=================================*/
.loginformado,
.loginempresa {
  position: absolute;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 150px 0px;
  width: 100%;
  height: 100%;
}

.loginformado ul li,
.loginempresa ul li {
  margin: 30px;
}

.loginformado ul li div input,
.loginempresa ul li input {
  padding: 12px 200px 12px 20px;
}

.loginformado button,
.loginempresa button {
  margin: 100px 0px;
  font-size: 1.5rem;
  font-weight: normal;
}

.loginformado h1,
.loginempresa h1 {
  font-size: 3rem;

}

.loginformado img,
.loginempresa img {
  margin: 300px 0px 60px 0px;
}

/*=================================
                Home
=================================*/
.home {
  position: absolute;
  margin: 100px;
  display: flex;

}
.home .criarpublicacao {
  display: flex;
  margin: 70px 35px;

}
.home .criarpublicacao input{
background: transparent;
border-style: NONE;
  padding: 28px 427px 28px 20px;
  color: #fff;
  border-radius: 30px;
  font-size: 18px;
}
.home .criarpublicacao{
  border-radius: 20PX;
  margin: 60px 800px 0px 35px;
  border-radius: 38px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 30px;
  border: solid 1px rgba(192, 192, 192, 0.233);

}
.home .criarpublicacao img{
  margin: 10px 0px 0px 620px;
  position: absolute;
  height: 80px;
}
.home div{
  align-items: center;
}
.home .p{
  display: flex;
  border-radius: 20PX;
  margin: 20px 800px 0px 35px;
  border-radius: 38px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 30px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 10px;
}
.home ul{
  display: flex;
  align-items: center;
  text-align: center;
}
.home h2{
  font-size: 25px;
  margin:10px 10px 10px 10px;
}
.home .pi{
  margin: 0px 0px 160px 0px;
}
.home p{
  max-width: 600px;
  margin: 0px 0px 0px 10px;
  line-height: 1.4;
}.home ul li.demais{
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 15px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 13px;
  margin: 10px;
}
.curriculo2{
  flex-direction: column;

}.curriculo2 ul{
 align-items: center;
 text-align: center;
}.curriculo{
  margin: 0px 200px 0px -600px;
}.curriculo div{
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 15px;
  border: solid 1px rgba(228, 221, 221, 0.233);
  padding: 20px;
  margin: 10px;
}.curriculo div img{
  position: absolute;
  margin: -40px 0px 0px 320px;
}.curriculo p{
  padding:40px 1px;
  line-height: 1.8;
  font-size: 18px;

}.curriculo .nell{
  padding: 30px 5px;
  margin:60px 0px ;
}.curriculo .curriculum{
   margin: -66px 0px 0px 340px ;
}.curriculo .curriculum2{
   margin: -66px 0px 0px 336px ;
}.curriculo .lembretes{
  padding: 0px;
  margin: 20px 20px 30px 0px;
}.curriculo .lembretes p{
  padding: 20px;
}
/*=============================
            Buscas
==============================*/
.buscas{
  position: absolute;
  margin: 130px;
  display: flex;
}
.buscas ul{
  display: flex;
  align-items: center;
}.buscas .es{
  flex-direction: column;
}.buscas div{
   border-radius: 38px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 15px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 10px;
  margin: 10px;
}.buscas .branco{
  background: #d4d4d493;
  border-radius: 15px;
  padding: 10px 100px 50px 10px;
  margin: 11px ;

}.buscas .branco2{
  background: #d4d4d493;
  border-radius: 15px;
  padding: 10px 10px 50px 10px;
  margin: 11px ;
}.buscas h2{
  color:#151592;
  margin: 10px 20px;
  font-size: 18px;
}.buscas p{
  color: #000;
  margin: 0px 10px 0px 10px;
  max-width: 600px;
  line-height:1.4 ;
}.buscas img{
  width: 60px;
  height: 60px;
  margin: 0px 0px 10px 0px;
}.buscas .esbranco{
    display: flex;
    align-items: center;
    text-align: left;
    margin: 0px 340px 0px 0px;
    justify-content: center;
}.buscas button{
  padding: 20px 180px;
  border-radius: 5px;
  margin: 20px;
  background: #0d0d36;
  color: #b1b1b1;
}.buscas .hsml{
  line-height: 2.0 ;
  margin: 10px 330px 10px 0px;
}.buscas .candidatar{
  margin: 10px;
  padding: 20px 215px;
}.buscas .ec{
  margin: 10px;
  padding: 20px 204px;
}
/*=============================
            Usuario
==============================*/
.usuario {
  position: absolute;
  margin: 150px;
}.usuario .agregar{
  align-items: center;
  display: flex;
  padding: 10px 10px 10px 10px;
   border-radius: 30px;

}.usuario button{
  border-radius: 38px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 15px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 10px;
  margin: 10px;
  color: #e7e7e7;
  padding: 22px 45px;
}.usuario img{
  width: 60px;
  height: 60px;
}.usuario .agregar p{
  margin: 0px 928px 0px 40px;


}.usuario .ana{
  border-radius: 38px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border-radius: 15px;
  border: solid 1px rgba(192, 192, 192, 0.233);
  padding: 10px;
  margin: 10px;
  color: #e7e7e7;
  padding: 22px 45px;
}.usuario p{
   line-height: 1.4;
   margin: 0px 0px 0px 14px;
}.usuario  h2{
  font-size: 20px;
  margin: 10px;
}.usuario .vs{
  margin: 0px 0px 0px 300px;
}.usuario .localidade{
align-items: center;
  padding: 10px 10px 10px 10px;
   border-radius: 30px;
   display: flex;
}.usuario .localidade p{
  margin: 0px 1000px 0px 40px;
}
/*=============================
          habilidades
==============================*/
.habilidades{
    position: absolute;
    margin:180px 200px;
    align-items: center;
    justify-content: center;
    text-align: center;


}.habilidades ul li{
  display: flex;
  align-items: center;
}.habilidades button{
  padding: 10px 10px 10px 330px;
  display: flex;
  align-items: center;
  margin: 10px;
  border-radius: 10px;
  background: #121245;
  color: #e7e7e7;

}.habilidades img{
  width: 60px;
  height: 60px;
  margin: 0px 0px -5px 220px;
}.habilidades div{
   border-radius: 38px;
  background: linear-gradient(130deg,
      rgba(255, 255, 255, 0.02) 19.68%,
      rgba(255, 255, 255, 0.1) 72.77%);
  box-shadow:
    -7px -9px 26.1px 0px rgba(255, 255, 255, 0.08) inset,
    7px 9px 19.6px 0px rgba (0, 0, 0, 0.2) inset;
  border: solid 1px rgba(192, 192, 192, 0.233);
  margin: 0px;
  color: #e7e7e7;
  padding: 44px 190px;
}.habilidades .hb{
  padding: 20px 310px;
   background: #31318F;
   border-radius: 10px ;
  color: #e7e7e7;
}.habilidades h2{
  font-size: 18px;
  margin: 10px 0px 10px 100px;
  color:#000 ;
}.habilidades .branco{
  padding: 20px;
  background: #d4d4d493;
  border-radius:10px ;

}.habilidades .hqv{
  padding: 0px;
  margin: 0px -140px 0px 100px;
}


/*=============================
            FOOTER
==============================*/
footer {
  background: #0d0d36;
  color: #fff;
  padding: 50px 5% ;
  display: flex;
  align-items: center;
  gap: 40px;
  font-family: 'Poppins', sans-serif;
  position: relative;
  justify-content: space-between;
}

footer ul {
  list-style: none;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
  padding: 0;
  margin: 0;
  align-items: center;
}

footer ul li a svg {
  width: 50px;
  height: 50px;
  fill: #fff;
  transition: fill 0.3s ease, transform 0.3s ease;
}

footer ul li a svg:hover {
  fill: #b1b1b1;
  transform: scale(1.2);
}

footer .copy {
  text-align: center;
  font-size: 14px;
  color: #aaa;
}

footer .geral {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
}

footer .geral li p,
footer .geral li button {
  color: #fff;
  font-weight: 500;
  font-size: 26px;
  transition: color 0.3s ease;
}

footer .geral li p a {
  text-decoration: none;
  color: inherit;
}

footer .geral li p a:hover,
footer .geral li button:hover {
  color: #b1b1b1;
  cursor: pointer;
}

footer button {
  background:transparent;
  color: #0d0d36;
  padding: 8px 20px;
  border-radius: 20px;
  border: none;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.3s, transform 0.3s;
}

footer button:hover {
  background: transparent;
  transform: scale(1.05);
}footer p:hover{
  transform: scale(1.1);
}

/* Footer logo */
footer img {
  width: 120px;
  object-fit: contain;
  margin-top: 20px;
  filter: brightness(0) invert(1);
  transition: transform 0.3s ease;
}

footer img:hover {
  transform: scale(1.1);
}
footer div{
  display: flex;
}

/* Responsivo */
@media (max-width: 768px) {
  footer ul,
  footer .geral {
    flex-direction: column;
    gap: 20px;
    align-items: center;
  }
}

</style>
