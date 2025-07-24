<template>
  <div id="app">
    <h3>Capitúlo 6</h3>
    <h1>Componentes juntos são mais fortes</h1>
    <lv-busca></lv-busca>
    <lv-perfil></lv-perfil>
    <hr>
    <nav-bar></nav-bar>
    <time-component></time-component>
    <h3>6.1 Teste seu conhecimento</h3>
    <h4>Memorize a teoria</h4>
    <p>Dividir o projeto em partes no casos, cinco componentes
      1 - lista de categorias.
      2 - produtos em destaque.
      3 - últimos comentários.
      4 - menu superior.
      5 - barra de busca.
    </p>
    <h4>Na prática</h4>
    <p>Vamos criar compontentes para mostrar na tela postagens </p>
    <div>
      <PostList :posts="postagens" @postSelecionada="exibirConteudo" />
      <PostContent :conteudo="conteudoSelecionado" />
    </div>

  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import LvTime from './components/LvTime.vue'
import TimeComponent from './components/timeHour.vue'
import LvBusca from './components/LvBusca.vue'
import LvPerfil from './components/LvPerfil.vue'
import NavBar from './components/NavBar.vue'

import PostList from './components/PostList.vue'
import PostContent from './components/PostContent.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld,
    NavBar,
    LvBusca,
    LvPerfil,
    TimeComponent,
    PostList, 
    PostContent
  },data() {
    return {
      postagens: [
        { id: 1, titulo: 'Vue é mágico', conteudo: 'Vue.js facilita a criação de interfaces reativas.' },
        { id: 2, titulo: 'Componentização', conteudo: 'Dividir sua interface em componentes melhora a organização.' },
        { id: 3, titulo: 'Reatividade', conteudo: 'Vue possui reatividade por padrão via Proxy.' }
      ],
      conteudoSelecionado: ''
    }
  },
  methods: {
    exibirConteudo(conteudo) {
      this.conteudoSelecionado = conteudo
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
