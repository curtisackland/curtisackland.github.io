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
    githubLink: String,
    liveLink: String,
    images: Array,
  },
};
</script>

<template>
  <a>
    <div class="card-container hover-shadow-effect">
      <h1 class="resume-header">
        {{ projectTitle }}
      </h1>
      <div class="links">
        <h2 class="date">{{ date }}</h2>
        <a
          v-if="githubLink"
          :href="githubLink"
          target="_blank"
          class="hover-highlight-effect"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 16 16"
            fill="currentColor"
            style="border-radius: 50%"
            class="link-icons hover-shadow-effect"
          >
            <path
              d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
            ></path>
          </svg>
        </a>
        <button v-if="liveLink" class="live-app-button hover-shadow-effect">
          <a class="live-app-link" :href="liveLink" target="_blank">
            Live App
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
          </a>
        </button>
      </div>
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
    }
  }
}

@keyframes slideTopRight {
  0% {
    transform: translateX(0) translateY(0);
  }
  100% {
    transform: translateX(4px) translateY(-4px);
  }
}

@keyframes slideBottomLeft {
  0% {
    transform: translateX(4px) translateY(-4px);
  }
  100% {
    transform: translateX(0) translateY(0);
  }
}

.arrows {
  height: 30px;
  width: auto;
}

.links {
  display: flex;
  flex-wrap: wrap;
  justify-items: center;
  align-content: center;
  align-items: center;
}

.link-icons {
  height: 30px;
  width: auto;
  margin: 4px 4px 4px 4px;
}

.live-app-button {
  background-color: rgba(255, 165, 0, 0.05);
  border-color: $accentColor;
  color: $accentColor;
  border-radius: 10px;
  font-size: 1.2em;
  padding: 16px;
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 30px;
  margin: 4px;

  &:hover {
    a {
      color: $accentColor;
    }

    svg {
      animation: slideTopRight 0.3s forwards;
    }
  }

  &:not(:hover) {
    svg {
      animation: slideBottomLeft 0.3s forwards;
    }
  }
}

@media (max-width: 250px) {
  .live-app-button {
    font-size: 1em;
  }
}

.live-app-link {
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  gap: 0.3rem;
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
  margin: 8px 4px 8px 4px;
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
