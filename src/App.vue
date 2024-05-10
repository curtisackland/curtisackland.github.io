<template>
  <nav>
    <a class="active" href="#Home"><h2>C</h2></a>
    <div class="links" id="links">
      <a href="javascript:void(0);" class="icon" @click="toggleNavBar()">
        <i class="mdi mdi-menu navbar-symbol"></i>
      </a>
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
    <div
      v-if="isNavBarOpen"
      class="open-responsive-navbar"
      @click="closeNavBar()"
    >
      <a
        href="javascript:void(0);"
        class="responsive-menu-toggle"
        @click="toggleNavBar()"
      >
        <i class="mdi mdi-close-circle-outline navbar-symbol"></i>
      </a>
      <a
        v-for="(item, index) in sections"
        :key="index"
        class="responsive-nav-items"
        :class="{ active: currentSection === item }"
        :href="'#' + item"
        @click="updateCurrentSection(item)"
      >
        {{ item }} &nbsp;
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
          class="arrows"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M3 10a.75.75 0 01.75-.75h10.638L10.23 5.29a.75.75 0 111.04-1.08l5.5 5.25a.75.75 0 010 1.08l-5.5 5.25a.75.75 0 11-1.04-1.08l4.158-3.96H3.75A.75.75 0 013 10z"
            clip-rule="evenodd"
          ></path>
        </svg>
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
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  box-sizing: border-box;
  padding: 30px;
  text-align: center;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;

  a {
    font-size: 1.2em;
    font-weight: bold;
    margin: 0 8px 0 8px;
    text-align: left;

    &.active {
      color: $accentColor;
    }
  }

  a:hover {
    color: $accentColor;
  }
}

.links {
  display: flex;
  align-items: center;

  & .icon {
    display: none;
  }
}

.navbar-symbol {
  font-size: 2.5em;
}

@media screen and (max-width: 700px) {
  nav {
    justify-content: space-between;
  }
  .links a {
    display: none;
  }
  .links a.icon {
    float: right;
    display: block;
  }
  .links {
    flex-direction: column;
  }
  .open-responsive-navbar {
    width: 100vw;
    height: 100vh;
    position: fixed;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: $backgroundColor;
    z-index: 100;
    left: 0;
    top: 0;

    a {
      margin: 0 0 24px;
      font-size: 2em;
    }
  }
}

.responsive-menu-toggle:hover {
  color: $accentColor;
}

.responsive-nav-items {
  display: flex;
  flex-wrap: wrap;
  white-space: normal;
  justify-content: center;
  align-items: center;
  text-align: center;

  &:hover {
    color: $accentColor;
    svg {
      animation: slideRight 0.3s forwards;
    }
  }

  &:not(:hover) {
    svg {
      animation: slideLeft 0.3s forwards;
    }
  }
}

@keyframes slideRight {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(25px);
  }
}

@keyframes slideLeft {
  0% {
    transform: translateX(25px);
  }
  100% {
    transform: translateX(0);
  }
}

.arrows {
  height: 30px;
  width: auto;
}

h2 {
  color: $accentColor;
  font-size: 2em;
  display: flex;
  align-items: center;
  text-align: center;
  justify-content: center;
  border: 2px solid $accentColor;
  border-radius: 5px;
  height: 1.5em;
  aspect-ratio: 1 / 1;
  margin: 0;
}

.home {
  align-content: center;
  min-height: 100vh;
}

@media screen and (max-width: 400px) {
  .home {
    padding-top: 130px; /* add space for nav bar */
  }
}

.section {
  margin-bottom: 25px;
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

      if (this.isNavBarOpen) {
        this.toggleNavBar();
      }
    },
    toggleNavBar() {
      this.isNavBarOpen = !this.isNavBarOpen;
    },
    closeNavBar() {
      this.isNavBarOpen = false;
    },
  },
  data() {
    return {
      currentSection: "Home",
      isNavBarOpen: false,
      sections: ["Home", "Resume", "Experience", "Projects", "Contact Me"],
    };
  },
  mounted() {
    document.title = "Curtis Ackland";
  },
};
</script>
