<template>
  <nav>
    <ul>
      <li>
        <NuxtLink to="/">Accueil </NuxtLink>
      </li>
      <li>
        <NuxtLink to="/favoris">Favoris</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/Astre">Page de l'Astre</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
nav {
  padding: 0 1rem;
}

nav ul {
  list-style-type: none;
  padding: 0;
  display: flex;
  justify-content: center;
}

nav ul li {
  padding: 1rem;
  font-size: 1.2rem;
}
</style>
