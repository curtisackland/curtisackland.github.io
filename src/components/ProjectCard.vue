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
    <div class="card-container hover-shadow-effect">
      <h1 class="resume-header">
        {{ projectTitle }}
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
          class="arrows"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M5.22 14.78a.75.75 0 001.06 0l7.22-7.22v5.69a.75.75 0 001.5 0v-7.5a.75.75 0 00-.75-.75h-7.5a.75.75 0 000 1.5h5.69l-7.22 7.22a.75.75 0 000 1.06z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </h1>
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

  &:hover {
    & .resume-header {
      color: $accentColor;
      svg {
        animation: slideTopRight 0.3s forwards;
      }
    }
  }

  &:not(:hover) {
    svg {
      animation: slideBottomLeft 0.3s forwards;
    }
  }
}

@keyframes slideTopRight {
  0% {
    transform: translateX(0) translateY(0);
  }
  100% {
    transform: translateX(10px) translateY(-10px);
  }
}

@keyframes slideBottomLeft {
  0% {
    transform: translateX(10px) translateY(-10px);
  }
  100% {
    transform: translateX(0) translateY(0);
  }
}

.arrows {
  height: 30px;
  width: auto;
}

.description {
  margin: 0;
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
