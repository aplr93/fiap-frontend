<template>
  <div v-if="post" class="post-container">
    <h1 class="post-title">{{ post.title }}</h1>
    <p class="post-content">{{ post.content }}</p>
    <button @click="goBack" class="btn">Voltar</button>
  </div>
  <div v-else class="post-container">
    <p>Post não encontrado.</p>
    <button @click="goBack" class="btn">Voltar</button>
  </div>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router';
import { posts } from '../data/posts';

const route = useRoute();
const router = useRouter();

const post = posts.find((p) => p.slug === route.params.slug);

const goBack = () => {
  router.back();
};
</script>

<style scoped>
.post-container {
  padding: 2rem;
  font-family: Arial, sans-serif;
}

.post-title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 700;
  color: #2c3e50;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
  margin-bottom: 1.5rem;
}

.post-content {
  font-size: 1.2rem;
  color: #444;
  line-height: 1.6;
  margin-bottom: 2rem;
}

.btn {
  display: inline-block;
  margin-top: 1rem;
  padding: 10px 20px;
  background-color: #e67e22;
  color: white;
  font-size: 16px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.btn:hover {
  background-color: #d35400;
  transform: scale(1.05);
}

.btn:active {
  transform: scale(0.98);
}
</style>



