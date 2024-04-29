<script>
export default {
  name: "BackToTopButton",
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
    handleScroll() {
      if (window.scrollY > 20) {
        this.showButton = true;
      } else {
        this.showButton = false;
      }
    },
  },
  data() {
    return {
      showButton: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<template>
  <i
    class="mdi mdi-arrow-up-bold-box hover-effect"
    style=""
    @click="scrollToTop"
    v-show="showButton"
    id="back-to-top"
  ></i>
</template>

<style scoped lang="scss">
#back-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 0;
  background-color: transparent;
  color: $accentColor;
  border: none;
  cursor: pointer;
  z-index: 1000;
}

#back-to-top:hover {
  color: $baseFontColor;
  animation: bounce 1s ease infinite;
}

#back-to-top::before {
  width: 100%;
  font-size: 64px;
}

@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-10px);
  }
  60% {
    transform: translateY(-5px);
  }
}
</style>
