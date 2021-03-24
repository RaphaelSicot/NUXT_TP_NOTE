<template>
  <div>
    <div class="navbar">
      <div><NuxtLink to="/">Accueil</NuxtLink></div>
      <div><NuxtLink to="/astre">Liste d'astres</NuxtLink></div>
      <div><NuxtLink to="/favorites">Mes favories</NuxtLink></div>
    </div>
    <Nuxt />
  </div>
</template>

<style scoped>
.navbar {
  background-color: #111827;
  display: flex;
  color: #fbbf24;
  font-family: "Courier New", Courier, monospace;
}

.navbar div {
  padding: 25px 15px 25px 15px;
}
</style>