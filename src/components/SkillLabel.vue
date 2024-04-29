<script>
export default {
  name: "SkillLabel",
  props: {
    name: String,
  },
};
</script>

<template>
  <div class="skill">{{ name }}</div>
</template>

<style scoped lang="scss">
.skill {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 100px;
  padding: 6px 10px 6px 10px;
  background-color: rgba(255, 165, 0, 0.1);
  color: $accentColor;
  margin: 0 4px 8px 4px;
}
</style>
