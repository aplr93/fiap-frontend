<template>
  <div class="blog-container">
    <h1 class="blog-title">
      <span class="blog-prefix">Blog dos alunos da FIAP</span>
      <span class="blog-names">Ana, Ayrton, Isabela e Rinaldo</span>
    </h1>
    <button class="btn" @click="createPost">Novo Post</button>
    <PostCard v-for="post in posts" :key="post.id" :post="post" />
  </div>
</template>

<script setup>
import { posts } from '../data/posts';
import PostCard from '../components/PostCard.vue';

const createPost = () => {
  alert('Função de criação de post ainda não implementada!');
};
</script>

<style scoped>
.blog-container {
  padding: 2rem;
  font-family: Arial, sans-serif;
}

.btn {
  display: inline-block;
  margin: 1rem 0;
  padding: 10px 20px;
  background-color: #e67e22;
  color: white;
  font-size: 16px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.btn:hover {
  background-color: #d35400;
  transform: scale(1.05);
}

.btn:active {
  transform: scale(0.98);
}

.blog-title {
  text-align: center;
  margin-bottom: 2rem;
  font-family: Arial, sans-serif;
  line-height: 1.4;
}

.blog-prefix {
  display: block;
  font-size: 2rem;
  font-weight: 700;
  color: #2c3e50;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
}

.blog-names {
  display: block;
  font-size: 1.5rem;
  font-weight: 500;
  color: #e67e22;
  margin-top: 0.2rem;
  text-shadow: 0.5px 0.5px 1px rgba(0,0,0,0.05);
}


</style>

