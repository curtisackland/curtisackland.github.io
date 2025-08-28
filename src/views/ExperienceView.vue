<script>
import ExperienceCard from "@/components/ExperienceCard.vue";

export default {
  name: "ExperienceView",
  components: { ExperienceCard },
};
</script>

<template>
  <div class="cards-container">
    <h1 class="experience-header">Experience</h1>
    <ExperienceCard
      job-title="Junior Software Engineer - Engineering Team"
      company="Zaui Software"
      date="July 2024 - Present"
      description="I build and maintain full-stack features for both customer-facing booking flows and internal tools used by travel and tour operators. My work includes developing scalable solutions, improving legacy systems, and collaborating across teams to deliver a seamless user experience."
      :skills="[
        'VueJS',
        'Vuetify',
        'Laravel',
        'PHP',
        'MySQL',
        'SCSS',
        'Blade templates',
        'Git',
        'Github',
        'Jira',
      ]"
      link="https://www.zaui.com/"
      class="card"
    ></ExperienceCard>
    <ExperienceCard
      job-title="Software Developer Intern - Digital Retailing Team"
      company="Mobials Inc/AutoVerify"
      date="May 2022 - August 2023"
      description="Developed software products for automotive dealers to generate leads in an
      Agile environment with a continuous integration and continuous development
      approach. Collaborated with the product team to understand product
      requirements. Collaborated with developers to mutually understand tasks
      and problems to efficiently resolve them."
      :skills="[
        'VueJS',
        'Vuetify',
        'Bootstrap',
        'Cypress',
        'Jest',
        'PHP Slim',
        'Doctrine',
        'MySQL',
        'PHPUnit',
        'Git',
        'Github',
      ]"
      link="https://www.autoverify.com/"
      class="card"
    ></ExperienceCard>
    <ExperienceCard
      job-title="Student Operator - Western Technology Services (WTS)"
      company="Western University"
      date="June 2021 - April 2022; September 2023 - April 2024"
      description="Executed, monitored, and troubleshooted daily batch requirements. Communicated with team to resolve issues and to minimize downtime."
      :skills="['Jenkins', 'Jira', 'PeopleSoft']"
      link="https://wts.uwo.ca/"
      class="card"
    ></ExperienceCard>
    <ExperienceCard
      job-title="Human Resources Assistant"
      company="Thames Valley District School Board"
      date="July - August 2018; July - August 2019"
      description="Electronic document management project: scanned, audited, and digitized confidential records; troubleshooted issues."
      :skills="[]"
      link="https://www.tvdsb.ca/"
      class="card"
    ></ExperienceCard>
    <ExperienceCard
      job-title="Produce Clerk"
      company="Sobeys North, London, Ontario"
      date="July 2017 – December 2021"
      description="Provided customer service, price verifications, maintained produce department stock, and trained new employees."
      :skills="[]"
      link="https://www.sobeys.com/"
      class="card"
    ></ExperienceCard>
  </div>
</template>

<style scoped lang="scss">
.cards-container {
  white-space: normal;
  justify-content: center;
  padding: 5% 25% 0 25%;
}

.experience-header {
  white-space: normal;
  justify-content: center;
  text-align: center;
  margin-bottom: 12px;
}

@media (max-width: 1250px) {
  .cards-container {
    padding: 5% 5% 0 5%;
  }
}

.card {
  margin: 0 0 16px;
}
</style>
