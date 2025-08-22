<script setup>
</script>

<template>
  <!--fundo do site-->
  <div class="background">
    <div class="degrade-top"></div>

    <div class="lado-esquerdo"></div>
    <div class="lado-direito"></div>
    <main class="mainpage">
      <section class="hero">
        <!-- Menu -->
        <div class="nav">
          <a href="#" class="text-white font-semibold drop-shadow">Vagas</a>
          <a href="#" class="text-white font-semibold drop-shadow">Empresas</a>
          <button>Login</button>
        </div>

        <!-- Texto principal -->
        <div class="intro-text">
          <p>
            Oi, somos o projeto IMT, um site com o propósito de apoiar os egressados na sua procura
            no âmbito laboral e empresas na busca de trabalhadores de qualidade. Se tua empresa está
            procurando vagas ou você é um egresso que começou no mundo do trabalho, faça o login e
            os ajudaremos na sua procura.
          </p>
          <p class="voce">Você é:</p>
        </div>

        <!-- Botões -->
        <div class="botoes-opcao">
          <button>Empresa</button>
          <button>Formado</button>
        </div>

        <!-- Título -->
        <h1>
          INTRODUÇÃO AO<br />
          MUNDO DO TRABALHO
        </h1>

      </section>
    </main>

    <div class="degrade-bottom"></div>
  </div>
</template>


<style scoped>
/*==============================================
                  background
===============================================*/
.background {
  background:rgba(8, 8, 30, 1);
  display: flex;
  height: 100vh;
  width: 100%;
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
  background: linear-gradient(to bottom, #08081E, rgba(8, 8, 30, 0));
  z-index: 1;
}

.degrade-bottom {
  bottom: 0;
  background: linear-gradient(to top, #08081E, rgba(8, 8, 30, 0));
}

.lado-esquerdo {
  width: 50%;
  background: conic-gradient(from 90deg at 50% 70%, #0c0c0c 0deg, #B1B1B1 110deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
}

.lado-direito {
  width: 50%;
  background: conic-gradient(from 90deg at 50% 70%, #0c0c0c 0deg, #B1B1B1 110deg, #f8f8f8 360deg);
  mix-blend-mode: color-dodge;
  height: 100%;
  transform: scaleX(-1);
}
/*======================================
                mainpage
=======================================*/
.mainpage {
  position: absolute;
  align-content: center;
  align-items: center;
}.hero{
  align-items: center;
  text-align:center ;
}

.nav{
  position: relative;
  z-index: 100;
  margin: 50px 0px 0px 60vw;
  align-content: start;

}

.nav a {
    z-index: 100;
    color: white;
}

a{

 font-size: 20px;
 text-decoration: none;
 padding: 0px 40px;
 /* color: #ffffff !important; força o branco */
a:hover {
    color: #ccccff; /* cor mais clara ao passar o mouse */
}
}p{
  color: #f8f8f8;
  margin: 40px 32vw 0px 32vw;
  line-height: 23px;
}button{
  padding: 10px 20px;
  border-radius: 20px;
  border-style: none;
  margin: 0px 0px 0px 25px;
}.botoes-opcao button{
  margin: 10px 60px;
}h1{
  font-size: 6vw;
  color: #b1b1b1;
  mix-blend-mode: color-dodge;
  margin: 100px 0px 0px 0px;

}.voce{
  margin: 10px;
}
</style>
