<template>
  <nav class="nav">
    <div class="logo">
      <img src="logo.png" alt="Logomarca">
    </div>
    <ul class="nav-links">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">Sobre</router-link></li>
      <li><router-link to="/contact">Contato</router-link></li>
    </ul>
    <button class="menu-button" @click="toggleMenu">☰</button>
    <ul class="menu" v-if="isMenuOpen">
      <li><router-link to="/services">Serviços</router-link></li>
      <li><router-link to="/blog">Blog</router-link></li>
      <li><router-link to="/support">Suporte</router-link></li>
    </ul>
  </nav>
</template>

<script>
export default {
    name: 'nav-bar',
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<style scoped>
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 20px;
  background: #333;
  color: white;
}

.logo img {
  height: 40px;
}

.nav-links {
  display: flex;
  gap: 15px;
  list-style: none;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

.menu-button {
  background: none;
  border: none;
  color: white;
  font-size: 24px;
  cursor: pointer;
}

.menu {
  display: flex;
  flex-direction: column;
  list-style: none;
  background: #444;
  padding: 10px;
  position: absolute;
  right: 20px;
  top: 50px;
}

.menu a {
  color: white;
  text-decoration: none;
  padding: 5px 0;
}
</style>
