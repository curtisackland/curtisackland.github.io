<template>
  <div class="home-container">
    <div>
      <h1>Curtis Ackland</h1>
      <img alt="Profile Picture" src="../assets/profile_picture.png" />
    </div>
    <div>
      <img alt="Profile Picture" src="../assets/profile_picture.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style lang="scss">
.home-container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

.profile-column {
  display: flex;
  flex-wrap: wrap;
}
</style>
