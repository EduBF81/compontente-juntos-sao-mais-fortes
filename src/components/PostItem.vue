<template>
  <li class="post-item" @click="selecionarPost">
    {{ postagem.titulo }}
  </li>
</template>

<script>
export default {
  name: 'PostItem',
  props: {
    postagem: {
      type: Object,
      required: true
    }
  },
  methods: {
    selecionarPost() {
      // Emite o conteúdo da postagem ao clicar
      this.$emit('postSelecionada', this.postagem.conteudo)
    }
  }
}
</script>

<style scoped>
.post-item {
  padding: 0.75rem;
  margin-bottom: 0.5rem;
  background-color: #f8f8f8;
  border: 1px solid #ddd;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.post-item:hover {
  background-color: #e6f0ff;
}
</style>
