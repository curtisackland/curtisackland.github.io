<script>
export default {
  name: "WebsiteInfo",
};
</script>

<template>
  <div class="info-container">
    <p>
      This website was coded and designed by me. It was built using
      <a href="https://vuejs.org/" target="_blank">Vue.js 3</a> and
      <a href="https://sass-lang.com/documentation/syntax/" target="_blank"
        >SCSS</a
      >
      and deployed to
      <a href="https://pages.github.com/" target="_blank">Github Pages</a> using
      <a href="https://github.com/features/actions" target="_blank"
        >Github Actions</a
      >.
    </p>
  </div>
</template>

<style scoped lang="scss">
.info-container {
  white-space: normal;
  justify-content: center;
  padding: 5% 25% 0 25%;
}

@media (max-width: 1250px) {
  .info-container {
    padding: 5% 5% 0 5%;
  }
}

a {
  color: $lighterFont;
}

a:hover {
  color: $accentColor;
}

p {
  text-align: center;
}
</style>
