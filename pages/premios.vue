<template>
  <main class="container">
    <PageTitle title="PREMIOS" />
    <section class="img-container">
      <img class="cine" src="~/static/img/premios/cartel-muestra-cine-premio.jpg" />
      <img src="~/static/img/premios/sin-alcohol-tram3.jpg" class="index-pic m-auto" />
      <img src="~/static/img/premios/laus-01-72ppp2.png" class="index-pic m-auto" />
    </section>
  </main>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding-bottom: 3rem;
}
img {
  margin: 0.2rem;
}
.cine {
  height: 25rem;
}
.img-container {
  display: flex;
}
</style>