<script>
export default {
  name: "ResumeView",
  methods: {
    updateResumePage(page) {
      this.page = page;
    },
  },
  data() {
    return {
      page: "Education",
      pages: [
        "Education",
        "Experience",
        "Technology",
        "Projects",
        "Hobbies",
        "Resume",
      ],
      technology: [
        "PHP",
        "HTML",
        "CSS",
        "SCSS",
        "JavaScript",
        "Java",
        "C++",
        "Qt5",
        "C",
        "C#",
        "Python",
        "PHP Slim",
        "PHPUnit",
        "Doctrine ORM",
        "Guzzle HTTP",
        "Twig",
        "RESTful API",
        "VueJS",
        "Vuetify",
        "Bootstrap",
        "Jest",
        "Cypress",
        "Python Flask",
        "Docker",
        "Git",
        "MySQL",
        "SQLite3",
        "PostgreSQL",
        "RabbitMQ",
        "Kafka",
        "Redis",
        "Maven",
        "AWS",
        "GCP",
        "IBM Cloud",
      ],
      hobbies: [
        {
          title: "Ball Hockey",
          description:
            "I enjoy playing ball hockey and I am currently playing in a local league.",
        },
        {
          title: "Basketball, Volleyball, and other sports",
          description:
            "Apart from the technology side of things, I enjoy playing a variety of sports and I enjoy watching basketball and hockey.",
        },
        {
          title: "Gaming",
          description:
            "I've been gaming since I was young, starting with Mario Kart on my brother's GameCube. Now, I enjoy playing a variety of competitive and adventure games on PC.",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="resume-container">
    <a
      href="https://drive.google.com/file/d/1Be7GE3HV6iK93Lf-EKbJ-VjZOLTUlqVu/preview"
      target="_blank"
    >
      <h1 class="resume-header">
        Resume
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
    </a>
    <div class="resume-buttons">
      <button
        v-for="(button, index) in pages"
        :key="index"
        :class="{ highlighted: page === button }"
        @click="updateResumePage(button)"
      >
        <h2>{{ button }}</h2>
      </button>
    </div>
    <div>
      <div v-if="page === 'Education'" class="education slide-in">
        <div style="display: flex; align-items: center">
          <img
            alt="Western University Crest"
            src="https://www.uwo.ca/img/homepage/2017/logo-western-crest-ftr.svg"
            style="
              width: 80px;
              float: left;
              margin-right: 12px;
              align-self: center;
            "
          />
          <div style="height: 100%; align-content: center">
            <p style="font-weight: bold">University of Western Ontario</p>
            <p>Honours Specialization in Computer Science</p>
            <p>Minor in Software Engineering</p>
          </div>
        </div>
        <div class="education-date">2019-2024</div>
      </div>
      <div v-else-if="page === 'Experience'" class="slide-in">
        <div class="education">
          <div>
            <p style="font-weight: bold">Software Developer Intern</p>
            <p>Mobials Inc./AutoVerify</p>
          </div>
          <div class="education-date">May 2022 - August 2023</div>
        </div>
        <div class="education">
          <div>
            <p style="font-weight: bold">
              Student Operator - Western Technology Services
            </p>
            <p>University of Western Ontario</p>
          </div>
          <div class="education-date">
            <p>June 2021 - April 2022</p>
            <p>Sept 2023 - April 2024</p>
          </div>
        </div>
        <div class="education">
          <div>
            <p style="font-weight: bold">Human Resources Assistant</p>
            <p>Thames Valley District School Board</p>
          </div>
          <div class="education-date">
            <p>July 2018 - August 2018</p>
            <p>July 2019 - August 2019</p>
          </div>
        </div>
        <div class="education">
          <div>
            <p style="font-weight: bold">Produce Clerk</p>
            <p>Sobeys</p>
          </div>
          <div class="education-date">July 2017 - December 2021</div>
        </div>
        <a href="#Experience">
          <h2 class="see-all-projects">
            See my experience &nbsp;
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
          </h2>
        </a>
      </div>
      <div v-else-if="page === 'Technology'" class="technology slide-in">
        <div
          v-for="(item, index) in technology"
          :key="index"
          style="
            display: flex;
            align-content: center;
            min-width: 125px;
            margin: 8px;
          "
        >
          <div class="bullet-point"></div>
          <span>{{ item }}</span>
        </div>
      </div>
      <div v-else-if="page === 'Projects'" class="slide-in">
        <div class="education">
          <div>
            <p class="project-titles">Rulemaking Influence Explorer</p>
          </div>
          <div class="education-date">September 2023 - April 2024</div>
        </div>
        <div class="education">
          <div>
            <p class="project-titles">Music Library Manager</p>
          </div>
          <div class="education-date">September 2023 - December 2023</div>
        </div>
        <div class="education">
          <div>
            <p class="project-titles">Flower Plant Recognizer</p>
          </div>
          <div class="education-date">May 2024</div>
        </div>
        <div class="education">
          <div>
            <p class="project-titles">Character Map Redesign</p>
          </div>
          <div class="education-date">January 2024 - April 2024</div>
        </div>
        <a href="#Projects">
          <h2 class="see-all-projects">
            See all projects &nbsp;
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
          </h2>
        </a>
      </div>
      <div v-else-if="page === 'Hobbies'" class="hobbies slide-in">
        <div
          v-for="(item, index) in hobbies"
          :key="index"
          style="display: flex; align-content: center; margin: 0 0 16px"
        >
          <div>
            <div class="bullet-point"></div>
          </div>
          <div style="margin-left: 8px">
            <p style="font-weight: bold">{{ item.title }}</p>
            <p>{{ item.description }}</p>
          </div>
        </div>
      </div>
      <div v-else-if="page === 'Resume'" class="slide-in hobbies">
        <iframe
          src="https://drive.google.com/file/d/1Be7GE3HV6iK93Lf-EKbJ-VjZOLTUlqVu/preview"
          style="width: 100%; height: auto; aspect-ratio: 0.77"
        >
        </iframe>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.resume-container {
  white-space: normal;
  justify-content: center;
  padding: 5% 25% 0 25%;
}

@media (max-width: 1250px) {
  .resume-container {
    padding: 5% 5% 0 5%;
  }
}

.resume-header {
  white-space: normal;
  justify-content: center;
  text-align: center;
  margin-bottom: 12px;

  &:hover {
    color: $accentColor;
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

.resume-buttons {
  display: flex;
  flex-wrap: wrap;
  width: 100%;

  button {
    flex: 1;
    padding: 12px 12px;
    background-color: transparent;
    color: $baseFontColor;
    border: 0;
    border-radius: 10px;
    cursor: pointer;
    min-width: 130px;

    &.highlighted {
      background-color: rgba(255, 165, 0, 0.1);
      color: $accentColor;
    }
  }

  button:hover {
    background-color: rgba(255, 255, 255, 0.1);
  }
}

.education {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-bottom: 12px;
}

p {
  margin: 0;
}

.education-date {
  align-content: center;
}

h2 {
  margin: 0;
}

.arrows {
  height: 30px;
  width: auto;
}

.bullet-point {
  border-radius: 50%;
  background-color: $accentColor;
  box-sizing: border-box;
  height: 10px;
  width: 10px;
  margin: 8px;
}

.technology {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 50px 0 !important;
}

.project-titles {
  font-weight: bold;
}

.hobbies {
  padding: 50px 5% !important;
}

.see-all-projects {
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

li::marker {
  color: $accentColor;
  font-size: 24px;
  height: 100%;
}

.slide-in {
  padding: 50px;
  animation: slideIn 0.5s ease forwards;
  opacity: 0;
  transform: translateX(-100%);
}

@keyframes slideIn {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
