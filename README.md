# Plataforma de Conexão entre Empresas e Formados

Este projeto é uma aplicação **front-end desenvolvida em Vue 3 + Vite** que tem como objetivo **aproximar empresas e profissionais formados**, criando uma interface simples, interativa e funcional para cadastro e login de ambos os lados.

A ideia principal é oferecer um espaço onde:

* **Empresas** possam se cadastrar, acessar sua conta e gerenciar informações.
* **Formados** possam criar perfis, acessar oportunidades e se conectar com empresas.

---

## Destaques do Projeto

* **Single Page Application (SPA)** → Navegação fluida sem recarregar a página.
* **Vue 3 + Vite** → Framework moderno e rápido, com build otimizada.
* **Interface customizada com CSS** → Responsiva, organizada com flexbox e grid.
* **Componentização** → Estrutura modular, facilitando expansão futura.
* **Ambiente de desenvolvimento prático** → Hot reload imediato, build leve e lint configurado.

---

## Funcionalidades Implementadas

* **Página Inicial (Home)** → Tela de apresentação e ponto de entrada.
* **Login de Formados** → Área exclusiva para acesso de profissionais já cadastrados.
* **Cadastro de Formados** → Criação de perfis de usuários formados.
* **Login de Empresas** → Acesso para empresas previamente registradas.
* **Cadastro de Empresas** → Registro de novas empresas interessadas em contratar formados.

A navegação entre essas páginas acontece de forma **reativa** através de variáveis de estado (`ref`), controladas pelo componente principal (`App.vue`).

---

## Estrutura do Projeto

```
📂 src/
 ├── 📄 App.vue          # Componente raiz com a lógica de navegação
 ├── 📂 components/      # Componentes reutilizáveis (header, footer, formulários etc.)
 ├── 📂 assets/          # Estilos, imagens e arquivos estáticos
 └── 📂 views/           # Telas principais (Home, Login, Cadastro)
```

---

## Tecnologias Utilizadas

* **Vue 3** → Framework JavaScript progressivo e reativo.
* **Vite** → Build tool rápida e moderna.
* **JavaScript (ES6+)** → Linguagem principal do projeto.
* **HTML5 & CSS3** → Estrutura e estilização.
* **ESLint** → Padronização e qualidade do código.

---

## Como Executar o Projeto

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

### 2️⃣ Instale as dependências

```bash
npm install
```

### 3️⃣ Ambiente de desenvolvimento

```bash
npm run dev
```

O projeto estará disponível em: `http://localhost:5173`

### 4️⃣ Build para produção

```bash
npm run build
```

### 5️⃣ Lint do código

```bash
npm run lint
```

---

## Objetivo do Site

Este projeto foi criado com a missão de **facilitar a conexão entre empresas e profissionais recém-formados**.
Ele pode ser expandido futuramente para incluir:

* Painel administrativo para empresas.
* Área de perfil para formados.
* Integração com banco de dados e API.
* Filtros e busca de oportunidades.

---

## Encerramento

Este projeto marca o início de uma plataforma voltada para conectar empresas e profissionais formados, construída com Vue 3 para garantir leveza, rapidez e escalabilidade.

Ele ainda pode ser expandido com novas funcionalidades, mas já demonstra:
* Organização do código
* Boas práticas de desenvolvimento front-end
* Estrutura clara e adaptável

Se você chegou até aqui, muito obrigado por conferir o projeto!