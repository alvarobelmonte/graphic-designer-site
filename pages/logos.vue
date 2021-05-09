<template>
  <main class="container-logos">
    <TheDialog
      :show="modalOpened"
      :image="modalImg"
      @close="closeModal"
      :description="modalDescription"
    />
    <PageTitle title="logos" />
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
      <div class="item item--10" @click="showModal(9)">
        <img :src="getImage(9)" />
      </div>
      <div class="item item--11" @click="showModal(10)">
        <img :src="getImage(10)" />
      </div>
      <div class="item item--12" @click="showModal(11)">
        <img :src="getImage(11)" />
      </div>
      <div class="item item--13" @click="showModal(12)">
        <img :src="getImage(12)" />
      </div>
      <div class="item item--14" @click="showModal(13)">
        <img :src="getImage(13)" />
      </div>
      <div class="item item--15" @click="showModal(14)">
        <img :src="getImage(14)" />
      </div>
      <div class="item item--16" @click="showModal(15)">
        <img :src="getImage(15)" />
      </div>
      <div class="item item--17" @click="showModal(16)">
        <img :src="getImage(16)" />
      </div>
      <div class="item item--18" @click="showModal(17)">
        <img :src="getImage(17)" />
      </div>
    </div>
  </main>
</template>

<script>
import images from "../static/logos";

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
      this.modalOpened = true;
      this.modalDescription = images[i].description;
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
  width: 50%;

  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  grid-template-rows: repeat(9, 1fr);
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
    grid-row: 1/2;
    grid-column: 1/2;
  }
  &--2 {
    grid-row: 1/4;
    grid-column: 2/5;
  }
  &--3 {
    grid-row: 2/3;
    grid-column: 1/2;
  }
  &--4 {
    grid-row: 3/4;
    grid-column: 1/2;
  }
  &--5 {
    grid-row: 1/2;
    grid-column: 5/6;
  }
  &--6 {
    grid-row: 2/3;
    grid-column: 5/6;
  }
  &--7 {
    grid-row: 3/4;
    grid-column: 5/6;
  }
  &--8 {
    grid-row: 4/7;
    grid-column: 1/4;
  }
  &--9 {
    grid-row: 4/6;
    grid-column: 4/6;
  }
  &--10 {
    grid-row: 6/7;
    grid-column: 4/5;
  }
  &--11 {
    grid-row: 6/7;
    grid-column: 5/6;
  }
  &--12 {
    grid-row: 7/8;
    grid-column: 1/2;
  }
  &--13 {
    grid-row: 8/9;
    grid-column: 1/2;
  }
  &--14 {
    grid-row: 9/10;
    grid-column: 1/2;
  }
  &--15 {
    grid-row: 7/10;
    grid-column: 2/5;
  }
  &--16 {
    grid-row: 7/8;
    grid-column: 5/6;
  }
  &--17 {
    grid-row: 8/9;
    grid-column: 5/6;
  }
  &--18 {
    grid-row: 9/10;
    grid-column: 5/6;
  }
}
</style>
