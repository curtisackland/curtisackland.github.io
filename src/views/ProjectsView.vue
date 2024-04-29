<script>
import ExperienceCard from "@/components/ExperienceCard.vue";

export default {
  name: "ProjectsView",
  components: { ExperienceCard },
};
</script>

<template>
  <div class="cards-container">
    <h1 class="projects-header">Projects</h1>
    <ExperienceCard
      job-title="Rulemaking Influence Explorer"
      company="Academic Project"
      date="September 2023 - April 2024"
      description="Collaborated with client (University Professor) to build a website designed to explore data
      obtained from the US Federal Register to better understand the relationships in rulemaking.
      Used VueJS with Vuetify, Bootstrap, and Axios to create an appealing and responsive user interface to browse through data.
      Used PHP Slim to build back-end endpoints that query an SQLite database based on user parameters and return the resulting data."
      :skills="[
        'VueJS',
        'Vuetify',
        'Bootstrap',
        'Selenium',
        'PHP Slim',
        'MySQL',
        'Docker',
        'Python',
      ]"
      link="https://github.com/curtisackland/rule-influence-website"
      class="card"
    ></ExperienceCard>
    <ExperienceCard
      job-title="Music Library Manager"
      company="Academic Project"
      date="September 2023 - December 2023"
      description="Utilized Spotify’s and Apple Music’s API to manipulate user playlists.
      Utilized a service-oriented architecture to ensure application continuity despite service disruptions or removal.
      Created custom shuffling and sorting algorithms and the ability for users to transfer playlists from one platform to another.
      Used VueJS for the front-end and Python Flask for the back-end. Used Docker to containerize the application and deploy it to IBM Cloud."
      :skills="['VueJS', 'Bootstrap', 'Python Flask', 'Docker', 'IBM Cloud']"
      link="https://github.com/curtisackland/music-library-manager"
      class="card"
    ></ExperienceCard>
    <ExperienceCard
      job-title="Character Map"
      company="Academic Project"
      date="January 2024 - April 2024"
      description="A redesign of Windows' Character Map built using VueJS with Vuetify and Bootstrap."
      :skills="['VueJS', 'Vuetify', 'Bootstrap', 'HTML', 'CSS', 'Javascript']"
      link="https://github.com/curtisackland/character-map"
      class="card"
    ></ExperienceCard>
  </div>
</template>

<style scoped lang="scss">
.cards-container {
  white-space: normal;
  justify-content: center;
  padding: 2% 25% 0 25%;
}

@media (max-width: 1250px) {
  .cards-container {
    padding: 5% 5% 0 5%;
  }
}

.card {
  margin: 0 0 16px;
}

.projects-header {
  white-space: normal;
  justify-content: center;
  text-align: center;
  margin-bottom: 12px;
}
</style>
