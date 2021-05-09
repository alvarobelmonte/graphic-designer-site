<template>
  <nav class="navbar">
    <div class="logo">
      <nuxt-link to="/">toni belmonte gráfico</nuxt-link>
    </div>
    <ul class="nav-items">
      <li class="nav-item">
        <nuxt-link to="/bio">bio</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/premios">premios</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/cartel">cartel</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/logos">logos</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/ilustracion">ilustración</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/editorial">editorial</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/calendarios">calendarios</nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link to="/contacto">contacto</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
.navbar {
  position: fixed;
  z-index: 20;
  width: 100%;
  background-color: black;
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
}
.logo {
  padding: 1rem 3rem;
  font-weight: bold;
  font-size: 1.7rem;
}
.nav-items {
  padding: 1rem 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-item {
  margin-right: 1rem;
  font-size: 1.2rem;
  font-weight: bold;
}

.nav-item:hover {
  color: rgb(255, 29, 180);
}

.nav-item .nuxt-link-active {
  color: rgb(255, 29, 180);
}

/********************** MOBILE **********************/
@media screen and (max-width: 1024px) {
  .navbar {
    flex-direction: column;
  }
  .nav-item {
    font-size: 0.9rem;
    margin-right: 0.5rem;
  }
}
@media screen and (max-width: 500px) {
  .navbar {
    flex-direction: column;
  }
  .nav-items {
    flex-direction: column;
  }
}
</style>