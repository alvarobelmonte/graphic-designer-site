<template>
  <h1 class="title">{{title}}</h1>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style scoped>
.title {
  font-size: 2.5rem;
  font-weight: bold;
  padding-bottom: 1rem;
}
</style>