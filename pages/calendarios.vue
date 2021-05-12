<template>
  <main class="container-logos">
    <TheDialog
      :show="modalOpened"
      :image="modalImg"
      @close="closeModal"
      :description="modalDescription"
    />
    <PageTitle title="calendarios" />
    <div class="grid-container">
      <div class="item item--1" @click="showModal(0)">
        <img :src="getImage(0)" />
      </div>
      <div class="item item--2" @click="showModal(1)">
        <img :src="getImage(1)" />
      </div>
      <div class="item item--3" @click="showModal(2)">
        <img :src="getImage(2)" />
      </div>
      <div class="item item--4" @click="showModal(3)">
        <img :src="getImage(3)" />
      </div>
      <div class="item item--5" @click="showModal(4)">
        <img :src="getImage(4)" />
      </div>
      <div class="item item--6" @click="showModal(5)">
        <img :src="getImage(5)" />
      </div>
      <div class="item item--7" @click="showModal(6)">
        <img :src="getImage(6)" />
      </div>
      <div class="item item--8" @click="showModal(7)">
        <img :src="getImage(7)" />
      </div>
      <div class="item item--9" @click="showModal(8)">
        <img :src="getImage(8)" />
      </div>
    </div>
  </main>
</template>

<script>
import images from "../static/calendarios";

export default {
  data() {
    return {
      modalOpened: false,
      modalImg: "",
      modalDescription: "",
    };
  },
  methods: {
    showModal(i) {
      this.modalImg = images[i].path;
      this.modalDescription = images[i].description;
      this.modalOpened = true;
    },
    closeModal() {
      this.modalOpened = false;
    },
    getImage(i) {
      return images[i].path;
    },
  },
};
</script>

<style scoped lang="scss">
::selection {
  color: none;
  background: none;
}
.container-logos {
  padding-bottom: 6rem;
  text-align: center;
}
img {
  width: 100%;
  height: 100%;
}
.grid-container {
  margin: 0 auto;
  width: 30%;

  display: grid;
  grid-template-columns: repeat(10, 1fr);
  grid-gap: 0.2rem;
}

@media screen and (max-width: 1024px) {
  .grid-container {
    width: 90%;
  }
}

.item {
  transition: all 0.3s;
  &:hover {
    transform: scaleX(1.03) scaleY(1.03);
  }
  &:hover {
    cursor: pointer;
  }

  &--1 {
    grid-row: span 2;
    grid-column: span 6;
  }
  &--2 {
    grid-row: span 1;
    grid-column: span 4;
  }
  &--3 {
    grid-row: span 1;
    grid-column: span 4;
  }
  &--4 {
    grid-row: span 1;
    grid-column: span 4;
  }
  &--5 {
    grid-row: span 2;
    grid-column: span 6;
  }
  &--6 {
    grid-row: span 1;
    grid-column: span 4;
  }
  &--7 {
    grid-row: span 1;
    grid-column: span 4;
  }
  &--8 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--9 {
    grid-row: span 1;
    grid-column: span 4;
  }
}
</style>
