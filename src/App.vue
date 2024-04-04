<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/experience">Experience</router-link> |
    <router-link to="/projects">Projects</router-link> |
    <router-link to="/resume">Resume</router-link> |
    <router-link to="/contact">Contact</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
nav {
  padding: 30px;
  text-align: center;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
<script setup></script>
