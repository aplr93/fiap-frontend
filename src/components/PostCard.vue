<template>
  <div class="post-card">
    <router-link :to="`/post/${post.slug}`" class="post-title">
      {{ post.title }}
    </router-link>
    <p class="post-description">{{ post.description }}</p>
    <hr class="divider" />
  </div>
</template>

<script setup>
defineProps({ post: Object });
</script>

<style scoped>
.post-card {
  margin-bottom: 1.5rem;
  padding: 1rem;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.3s ease;
  background-color: #fff;
}

.post-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.post-title {
  display: block;
  font-size: 1.25rem;
  font-weight: 600;
  color: #1e6fd9;
  text-decoration: none;
  margin-bottom: 0.5rem;
}

.post-title:hover {
  text-decoration: underline;
}

.post-description {
  color: #444;
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.divider {
  border: none;
  border-top: 1px solid #eee;
  margin-top: 1rem;
}
</style>

