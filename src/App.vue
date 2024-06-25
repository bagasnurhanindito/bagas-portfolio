<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWord.vue'
</script>

<template>
  <header>
    <div class="logo-container">
      <img alt="Vue logo" class="logo" src="@/assets/bagas.jpg" width="300" height="400" />
    </div>
    <div class="wrapper">
      <HelloWorld msg="Hallo, Saya Bagas Nur Hanindito" />
    </div>
  </header>

  <nav>
    <RouterLink to="/" exact>Beranda</RouterLink>
    <RouterLink to="/about">Tentang</RouterLink>
    <RouterLink to="/contact">Kontak</RouterLink>
  </nav>

  <RouterView />
</template>

<style scoped>
:root {
  --color-text: #333;
  --color-border: #ddd;
  --section-gap: 2rem;
  --color-bg: #f0f0f0;
  --color-primary: #42b983;
  --color-secondary: #35495e;
  --font-family: 'Arial, sans-serif';
}

body {
  font-family: var(--font-family);
  background-color: #433f3f;
  margin: 0;
  padding: 0;
}

header {
  display: flex;
  align-items: center;
  justify-content: center;
  line-height: 1.5;
  max-height: 100vh;
  background: url('https://wallpapercave.com/wp/wp2800904.jpg') no-repeat center center;
  background-size: cover;
  padding: var(--section-gap);
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  color: var(--color-text);
}

.logo-container {
  margin-right: var(--section-gap);
}

.logo {
  display: block;
  margin: 0 auto;
  border-radius: 50%;
  border: 5px solid var(--color-primary);
}

.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

nav {
  width: 100%;
  font-size: 14px;
  text-align: center;
  margin-top: 2rem;
  background-color: var(--color-secondary);
  padding: 1rem;
  border-radius: 8px;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  color: white;
  text-decoration: none;
  transition: color 0.3s ease, background-color 0.3s ease;
}

nav a.router-link-exact-active {
  color: var(--color-primary);
  font-weight: bold;
}

nav a:hover {
  background-color: var(--color-primary);
  color: white;
  border-radius: 4px;
}

@media (min-width: 1024px) {
  header {
    justify-content: flex-start;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0;
  }

  .wrapper {
    align-items: flex-start;
    text-align: left;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;
    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>