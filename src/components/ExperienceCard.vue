<script>
import SkillLabel from "@/components/SkillLabel.vue";

export default {
  name: "ExperienceCard",
  components: { SkillLabel },
  props: {
    jobTitle: String,
    company: String,
    date: String,
    description: String,
    skills: Array,
    link: String,
  },
};
</script>

<template>
  <a :href="link" target="_blank">
    <div class="card-container hover-shadow-effect">
      <h1>{{ jobTitle }} - {{ company }}</h1>
      <h2 class="date">{{ date }}</h2>
      <p>{{ description }}</p>
      <div class="skills-section">
        <SkillLabel
          v-for="item in skills"
          :key="item"
          :name="item"
        ></SkillLabel>
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
  margin-bottom: 16px;
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
</style>
