<template>
  <main>
    <div v-if="show" @click="tryClose" class="backdrop"></div>
    <transition name="dialog">
      <dialog open v-if="show">
        <div class="p-2 bg-white">
          <img :src="image" />
          <h2 class="bg-black text-yellow-200 p-2 w-full">{{description}}</h2>
        </div>
      </dialog>
    </transition>
  </main>
</template>

<script>
export default {
  props: {
    show: {
      type: Boolean,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: false,
    },
  },
  emits: ["close"],
  methods: {
    tryClose() {
      this.$emit("close");
    },
  },
};
</script>

<style scoped lang="scss">
.backdrop {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.75);
  z-index: 10;
}

dialog {
  position: fixed;
  top: 5vh;
  left: 10%;
  width: 80%;
  z-index: 100;
  border-radius: 12px;
  border: none;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 0;
  margin: 0;
  overflow: hidden;
  background-color: white;
  img {
    width: 90%;
    height: 90%;
    margin: 0 auto;
  }
}

.dialog-enter-from,
.dialog-leave-to {
  opacity: 0;
  transform: scale(0.8);
}

.dialog-enter-active {
  transition: all 0.1s ease-out;
}
.dialog-leave-active {
  transition: all 0.1s ease-in;
}

.dialog-enter-to,
.dialog-leave-from {
  opacity: 1;
  transform: scale(1);
}

@media (min-width: 768px) {
  dialog {
    left: calc(50% - 20rem);
    width: 40rem;
  }
}
</style>