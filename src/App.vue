<template>
  <nav>
    <a class="active" href="#home"><h2>C</h2></a>
    <div class="links">
      <a
        v-for="(item, index) in sections"
        :key="index"
        :class="{ active: currentSection === item }"
        :href="'#' + item"
        @click="updateCurrentSection(item)"
      >
        {{ item }}
      </a>
    </div>
  </nav>
  <HomeView id="Home" class="home section"></HomeView>
  <ResumeView id="Resume" class="section"></ResumeView>
  <ExperienceView id="Experience" class="section"></ExperienceView>
  <ProjectsView id="Projects" class="section"></ProjectsView>
  <ContactView id="Contact Me" class="section"></ContactView>
  <WebsiteInfo class="section"></WebsiteInfo>
  <BackToTopButton></BackToTopButton>
</template>

<style scoped lang="scss">
nav {
  padding: 30px;
  text-align: center;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;

  a {
    font-weight: bold;
    color: $baseFontColor;
    text-decoration: none;
    margin: 0 8px 0 8px;
    text-align: left;

    &.active {
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

.home {
  align-content: center;
  min-height: 100vh;
}

.section {
  margin-bottom: 100px;
}
</style>
<script>
import HomeView from "@/views/HomeView.vue";
import ExperienceView from "@/views/ExperienceView.vue";
import ProjectsView from "@/views/ProjectsView.vue";
import ResumeView from "@/views/ResumeView.vue";
import ContactView from "@/views/ContactView.vue";
import BackToTopButton from "@/components/BackToTopButton.vue";
import WebsiteInfo from "@/views/WebsiteInfo.vue";
export default {
  name: "App",
  components: {
    HomeView,
    ExperienceView,
    ProjectsView,
    ResumeView,
    ContactView,
    BackToTopButton,
    WebsiteInfo,
  },
  methods: {
    updateCurrentSection(section) {
      this.currentSection = section;
    },
  },
  data() {
    return {
      currentSection: "Home",
      sections: ["Home", "Resume", "Experience", "Projects", "Contact Me"],
    };
  },
};
</script>
