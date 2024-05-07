<script>
import SkillLabel from "@/components/SkillLabel.vue";

export default {
  name: "ProjectCard",
  components: { SkillLabel },
  props: {
    projectTitle: String,
    date: String,
    description: String,
    skills: Array,
    link: String,
    images: Array,
  },
};
</script>

<template>
  <a :href="link" target="_blank">
    <div class="card-container">
      <h1>{{ projectTitle }}</h1>
      <h2 class="date">{{ date }}</h2>
      <div class="skills-section">
        <SkillLabel
          v-for="item in skills"
          :key="item"
          :name="item"
        ></SkillLabel>
      </div>
      <p class="description">{{ description }}</p>
      <div>
        <img
          v-for="(item, index) in images"
          :key="index"
          :src="item"
          width="100%"
          :alt="projectTitle + ' images'"
          class="project-image"
        />
      </div>
    </div>
  </a>
</template>

<style scoped lang="scss">
.card-container {
  box-sizing: border-box;
  width: 100%;
  border-radius: 10px;
  border: 1px solid $accentColor;
  background-color: rgba(255, 165, 0, 0.05);
  padding: 16px;
  opacity: 0;
  animation: fadeIn 1s ease-out forwards;
}

.description {
  margin: 0;
}

a {
  text-decoration: none;
  color: $baseFontColor;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.date {
  margin: 8px 0 8px 0;
}

.skills-section {
  display: flex;
  flex-wrap: wrap;
}

.project-image {
  margin: 8px 0 0 0;
  border-radius: 4px;
}
</style>
