<template>
  <div v-if="conteudo" class="post-content">
    <h2>Conteúdo da Postagem</h2>
    <p>{{ conteudo }}</p>
  </div>
</template>

<script>
export default {
  name: 'PostContent',
  props: {
    conteudo: {
      type: String,
      required: false
    }
  }
}
</script>

<style scoped>
.post-content {
  padding: 1rem;
  margin-top: 1rem;
  background-color: #fffbe6;
  border-left: 5px solid #ffd24d;
  box-shadow: 0 0 6px rgba(0,0,0,0.1);
}

.post-content h2 {
  margin-bottom: 0.5rem;
}

.post-content p {
  font-size: 1rem;
  line-height: 1.5;
}
</style>
