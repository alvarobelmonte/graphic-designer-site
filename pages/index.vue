<template>
  <div class="container">
    <PageTitle title="HOLA" />
    <img src="~/static/img/index/index.jpg" class="index-pic m-auto" />
  </div>
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
}

.index-title {
  font-size: 3rem;
  font-weight: bold;
}

.index-pic {
  width: 30%;
}
@media screen and (max-width: 1024px) {
  .index-pic {
    width: 40%;
  }
}
@media screen and (max-width: 500px) {
  .index-pic {
    width: 60%;
  }
}
</style>
