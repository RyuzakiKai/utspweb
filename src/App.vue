<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
  <div class="container">
    <nav
        class="navbar navbar-expand-lg bg-body-tertiary-center"
    >
      <a class="navbar-brand" >القرآن</a>
      <router-link :class="{ active: $route.name === 'home' }" class="y nav-link" to="/home">Home</router-link>
      <router-link :class="{ active: $route.name === 'surah' }" class="y nav-link" to="/surah">Surah</router-link>
      <router-link :class="{ active: $route.name === 'about' }" class="y nav-link" to="/about" >About Al-Qur'an</router-link>
    </nav>
  </div>
</header>
  <RouterView/>
</template>

<style scoped>
.navbar-brand {
  color: rgb(0, 0, 0);
 font-size: 3rem;
}

.navbar-expand-lg {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  text-align: center;
  background-color: rgba(76, 187, 117, 0.96);
  margin-top: 60px;
  display: flex;
  justify-content: space-between;
  padding: 5px 10px ;

}
header {
  line-height: 1.5;
  max-height: 100vh;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
  color: red ;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: 1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
header{

}
</style>

