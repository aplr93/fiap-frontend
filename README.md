# Blog dos Alunos da FIAP

Este é um projeto de blog simples desenvolvido com [Vue 3](https://vuejs.org/), utilizando [Vite](https://vitejs.dev/) como bundler e [Vue Router](https://router.vuejs.org/) para navegação entre páginas.

## 👨‍💻 Integrantes

- Ana 
- Ayrton 
- Isabela 
- Rinaldo 

## 📂 Estrutura do Projeto

```
.
├── index.html
├── package.json
├── vite.config.js
├── /public
├── /src
│   ├── App.vue
│   ├── main.js
│   ├── router.js
│   ├── style.css
│   ├── /components
│   │   └── PostCard.vue
│   │   └── Loading.vue
│   │   └── Error.vue
│   ├── /data
│   │   └── posts.js
│   └── /views
│       ├── BlogView.vue
│       └── PostView.vue
```

## 🚀 Funcionalidades

- Exibição de posts simulados (mockados) via `data/posts.js`.
- Roteamento de páginas com `vue-router`.
- Interface responsiva e estilizada com CSS customizado.
- Página de lista de posts e visualização individual de cada post.

## 🛠️ Tecnologias Utilizadas

- [Vue 3](https://vuejs.org/)
- [Vite](https://vitejs.dev/)
- [Vue Router](https://router.vuejs.org/)

## 📦 Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/aplr93/fiap-frontend.git
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

## 📌 Observações

- A funcionalidade de **"Criar Post"** ainda não está implementada. Atualmente, ao clicar no botão, um alerta será exibido.
- Os dados dos posts estão sendo carregados de um arquivo local `data/posts.js`.

## 📄 Licença

Este projeto é apenas para fins educacionais.
