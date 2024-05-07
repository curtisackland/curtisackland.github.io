<script>
import ProjectCard from "@/components/ProjectCard.vue";

export default {
  name: "ProjectsView",
  components: { ProjectCard },
};
</script>

<template>
  <div class="projects-container">
    <h1 class="projects-header">Projects</h1>
    <div class="project-cards-container">
      <ProjectCard
        project-title="Rulemaking Influence Explorer"
        date="2023-2024"
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
        :images="[
          require('@/assets/projectImages/rulemakingInfluenceExplorer/homepage.png'),
        ]"
      ></ProjectCard>
      <ProjectCard
        project-title="Music Library Manager"
        date="2023"
        description="Utilized Spotify’s and Apple Music’s API to manipulate user playlists.
        Utilized a service-oriented architecture to ensure application continuity despite service disruptions or removal.
        Created custom shuffling and sorting algorithms and the ability for users to transfer playlists from one platform to another.
        Used VueJS for the front-end and Python Flask for the back-end. Used Docker to containerize the application and deploy it to IBM Cloud."
        :skills="['VueJS', 'Bootstrap', 'Python Flask', 'Docker', 'IBM Cloud']"
        link="https://github.com/curtisackland/music-library-manager"
        :images="[
          require('@/assets/projectImages/musicLibraryManager/music-library-manager.jpg'),
        ]"
      ></ProjectCard>
      <ProjectCard
        project-title="Apex Extermination: Lone Operative Game"
        date="2024"
        description="A 3D open-world first person shooter where the player must eliminate enemies and level up while they explore Area52 and defeat the 3 bosses. Built using C# and Unity."
        :skills="['C#', 'Unity']"
        link="https://github.com/curtisackland/4483-game"
        :images="[
          require('@/assets/projectImages/apexExterminationGame/apex-extermination.png'),
        ]"
      ></ProjectCard>
      <ProjectCard
        project-title="Character Map Redesign"
        date="2024"
        description="A redesign of Windows' Character Map built using VueJS with Vuetify and Bootstrap."
        :skills="['VueJS', 'Vuetify', 'Bootstrap', 'HTML', 'CSS', 'Javascript']"
        link="https://github.com/curtisackland/character-map"
        :images="[
          require('@/assets/projectImages/characterMapRedesign/character-map-redesign.png'),
        ]"
      ></ProjectCard>
      <ProjectCard
        project-title="Personal Portfolio Website"
        date="2024"
        description="A website showing off my personal portfolio. Built using VueJS."
        :skills="['VueJS', 'SCSS', 'HTML', 'CSS', 'Javascript']"
        link="https://github.com/curtisackland/curtisackland.github.io"
        :images="[
          require('@/assets/projectImages/personalPortfolioWebsite/personal-portfolio.png'),
        ]"
      ></ProjectCard>
      <ProjectCard
        project-title="Return of Monke Game"
        date="2021"
        description="2D top down shooter where the player plays as a monkey that has to defeat waves of monsters and survive as long as possible. This project was made in C++ using QT5 and Boost."
        :skills="['C++', 'QT5', 'Boost']"
        link="https://github.com/curtisackland/Return-Of-Monke"
        :images="[
          require('@/assets/projectImages/returnOfMonkeGame/return-of-monke-game.png'),
        ]"
      ></ProjectCard>
      <ProjectCard
        project-title="Country Demographic Analysis App"
        date="2020"
        description="Provides statistics about certain countries by retreiving information from the World Bank API and displaying it using various charts. Built in Java using Java Swing for the user interface and JFreeChart for the graphs."
        :skills="['Java', 'Java Swing', 'JFreeChart', 'Maven']"
        link="https://github.com/curtisackland/country-demographic-analysis"
        :images="[
          require('@/assets/projectImages/countryDemographicAnalysis/country-demographic-analysis.png'),
        ]"
      ></ProjectCard>
    </div>
  </div>
</template>

<style scoped lang="scss">
.projects-container {
  padding: 5% 0 0 0;
}

.project-cards-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(500px, 1fr));
  grid-auto-rows: min-content;
  gap: 20px;
  padding: 0 5% 0 5%;
}

@media (max-width: 600px) {
  .project-cards-container {
    grid-template-columns: repeat(auto-fill, 100%);
  }
}

.projects-header {
  white-space: normal;
  justify-content: center;
  text-align: center;
  margin-bottom: 12px;
}
</style>
