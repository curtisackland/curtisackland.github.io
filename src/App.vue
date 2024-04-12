<template>
  <nav>
    <router-link to="/">
      <h2>C</h2>
    </router-link>
    <div class="links">
      <router-link to="/">About</router-link>&nbsp;
      <router-link to="/experience">Experience</router-link>&nbsp;
      <router-link to="/projects">Projects</router-link>&nbsp;
      <router-link to="/resume">Resume</router-link>&nbsp;
      <router-link to="/contact">Contact</router-link>
    </div>
  </nav>
  <router-view />
</template>

<style lang="scss">
nav {
  padding: 30px;
  text-align: center;
  display: flex;
  justify-content: space-between;

  a {
    font-weight: bold;
    color: $baseFontColor;
    text-decoration: none;
    margin: 0 8px 0 8px;

    &.router-link-exact-active {
      color: $accentColor;
    }
  }
}

.links {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

h2 {
  color: $accentColor;
  margin: 0;
  font-size: 2em;
  display: flex;
  align-items: center;
  text-align: center;
  justify-content: center;
  border: 2px solid $accentColor;
  border-radius: 5px;
  height: 1.5em;
  aspect-ratio: 1 / 1;
}
</style>
