<template>
  <main class="container-logos">
    <TheDialog
      :show="modalOpened"
      :image="modalImg"
      @close="closeModal"
      :description="modalDescription"
    />
    <PageTitle title="cartel" />
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
      <div class="item item--19" @click="showModal(18)">
        <img :src="getImage(18)" />
      </div>
      <div class="item item--20" @click="showModal(19)">
        <img :src="getImage(19)" />
      </div>
      <div class="item item--21" @click="showModal(20)">
        <img :src="getImage(20)" />
      </div>
      <div class="item item--22" @click="showModal(21)">
        <img :src="getImage(21)" />
      </div>
      <div class="item item--23" @click="showModal(22)">
        <img :src="getImage(22)" />
      </div>
      <div class="item item--24" @click="showModal(23)">
        <img :src="getImage(23)" />
      </div>
      <div class="item item--25" @click="showModal(24)">
        <img :src="getImage(24)" />
      </div>
      <div class="item item--26" @click="showModal(25)">
        <img :src="getImage(25)" />
      </div>
      <div class="item item--27" @click="showModal(26)">
        <img :src="getImage(26)" />
      </div>
      <div class="item item--28" @click="showModal(27)">
        <img :src="getImage(27)" />
      </div>
      <div class="item item--29" @click="showModal(28)">
        <img :src="getImage(28)" />
      </div>
      <div class="item item--30" @click="showModal(29)">
        <img :src="getImage(29)" />
      </div>
      <div class="item item--31" @click="showModal(30)">
        <img :src="getImage(30)" />
      </div>
      <div class="item item--32" @click="showModal(31)">
        <img :src="getImage(31)" />
      </div>
    </div>
  </main>
</template>

<script>
import images from "../static/cartel";

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
  width: 25%;

  display: grid;
  grid-template-columns: repeat(12, 1fr);
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
    grid-row: span 1;
    grid-column: span 12;
  }
  &--2 {
    grid-row: span 1;
    grid-column: span 12;
  }
  &--3 {
    grid-row: span 1;
    grid-column: span 12;
  }
  &--4 {
    grid-row: span 1;
    grid-column: span 12;
  }
  &--5 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--6 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--7 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--8 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--9 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--10 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--11 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--12 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--13 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--14 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--15 {
    grid-row: span 2;
    grid-column: span 6;
  }
  &--16 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--17 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--18 {
    grid-row: span 2;
    grid-column: span 12;
  }
  &--19 {
    grid-row: span 2;
    grid-column: span 12;
  }
  &--20 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--21 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--22 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--23 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--24 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--25 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--26 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--27 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--28 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--29 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--29 {
    grid-row: span 1;
    grid-column: span 6;
  }
  &--30 {
    grid-row: span 1;
    grid-column: span 12;
  }
  &--31 {
    grid-row: span 1;
    grid-column: span 12;
  }
  &--32 {
    grid-row: span 1;
    grid-column: span 12;
  }
}
</style>
