<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
    <h3>
      Hallo Saya<br> Bagas Nur Hanindito, Hobby saya Futsal dan Otomotif
    </h3>
  </div>
</template>

<style scoped>
:root {
  --primary-color: #42b983;
  --secondary-color: #35495e;
  --accent-color: blueviolet;
  --background-color: #f9f9f9;
  --font-family: 'Arial, sans-serif';
}

.greetings {
  background-color: var(--background-color);
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  max-width: 600px;
  margin: 2rem auto;
  text-align: center;
  font-family: var(--font-family);
}

h1 {
  font-weight: 600;
  font-size: 2.6rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
  transition: transform 0.3s ease-in-out;
}

h1:hover {
  transform: scale(1.05);
}

h3 {
  font-size: 1.2rem;
  color: var(--accent-color);
  margin-top: 0;
}

@media (min-width: 1024px) {
  .greetings {
    text-align: left;
    padding: 3rem;
  }

  h1 {
    font-size: 3rem;
  }

  h3 {
    font-size: 1.5rem;
  }
}
</style>
