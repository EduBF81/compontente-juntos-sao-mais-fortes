<template>
  <ul>
    <PostItem
      v-for="post in posts"
      :key="post.id"
      :postagem="post"
      @postSelecionada="manipularClique"
    />
  </ul>
</template>

<script>
import PostItem from './PostItem.vue'

export default {
  name: 'PostList',
  props: {
    posts: {
      type: Array,
      required: true
    }
  },
  components: {
    PostItem
  },
  methods: {
    manipularClique(conteudo) {
      this.$emit('postSelecionada', conteudo)
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
</style>
