<template>
  <div class="home-container">
    <h4 class="nice-to-meet-you">Nice to meet you, my name is</h4>
    <h1 class="falling-text">
      <div>
        <span>C</span>
        <span>u</span>
        <span>r</span>
        <span>t</span>
        <span>i</span>
        <span>s&nbsp;</span>
      </div>
      <div>
        <span>A</span>
        <span>c</span>
        <span>k</span>
        <span>l</span>
        <span>a</span>
        <span>n</span>
        <span>d</span>
        <span>.</span>
      </div>
    </h1>
    <p class="about-me">
      I'm a Junior Software Engineer based in London, Ontario, Canada and an
      Honours Computer Science graduate from Western University. I build
      full-stack web applications using PHP/Laravel and Vue.js — from designing
      REST APIs and working with MySQL to building responsive, user-friendly
      interfaces. I’ve worked on both customer-facing features and internal
      tools, and I enjoy solving real-world problems through clean, maintainable
      code.
    </p>
    <div class="icons-space">
      <button class="contact-me-button link-icons hover-shadow-effect">
        <a class="mail-to-link" href="mailto: curtisackland@rogers.com">
          Email Me
        </a>
      </button>
      <div>
        <a
          href="https://github.com/curtisackland"
          target="_blank"
          class="hover-highlight-effect"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 16 16"
            fill="currentColor"
            class="link-icons"
          >
            <path
              d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
            ></path>
          </svg>
        </a>
      </div>
      <div>
        <a
          href="https://www.linkedin.com/in/curtis-ackland/"
          target="_blank"
          class="hover-highlight-effect"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="link-icons"
          >
            <path
              d="M20.5 2h-17A1.5 1.5 0 002 3.5v17A1.5 1.5 0 003.5 22h17a1.5 1.5 0 001.5-1.5v-17A1.5 1.5 0 0020.5 2zM8 19H5v-9h3zM6.5 8.25A1.75 1.75 0 118.3 6.5a1.78 1.78 0 01-1.8 1.75zM19 19h-3v-4.74c0-1.42-.6-1.93-1.38-1.93A1.74 1.74 0 0013 14.19a.66.66 0 000 .14V19h-3v-9h2.9v1.3a3.11 3.11 0 012.7-1.4c1.55 0 3.36.86 3.36 3.66z"
            ></path>
          </svg>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped lang="scss">
.home-container {
  white-space: normal;
  justify-content: center;
  padding: 0 25% 0 25%;
}

@media (max-width: 1000px) {
  .home-container {
    padding: 0 5% 0 5%;
  }
}

.icons-space {
  display: flex;
  flex-wrap: wrap;
}

.link-icons {
  height: 60px;
  width: auto;
  margin: 4px 4px 4px 4px;
}

.about-me {
  font-size: 1.2em;
  line-height: 200%;
}

.contact-me-button {
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
}

.mail-to-link {
  text-align: center;
  color: $accentColor;
}

.nice-to-meet-you {
  color: $accentColor;
  margin: 0;
}

/* for falling text */
.falling-text {
  display: flex;
  flex-wrap: wrap;
  font-size: 4em;
  white-space: normal;
}

.falling-text span {
  animation: falling-text 1s ease forwards;
  opacity: 0;
  transform: translateY(-50vh);
  display: inline-block;
}

@keyframes falling-text {
  0% {
    opacity: 0;
    transform: translateY(-50vh);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Delay each character */
.falling-text div:nth-child(1) span:nth-child(1) {
  animation-delay: 0.1s;
}
.falling-text div:nth-child(1) span:nth-child(2) {
  animation-delay: 0.2s;
}
.falling-text div:nth-child(1) span:nth-child(3) {
  animation-delay: 0.3s;
}
.falling-text div:nth-child(1) span:nth-child(4) {
  animation-delay: 0.4s;
}
.falling-text div:nth-child(1) span:nth-child(5) {
  animation-delay: 0.5s;
}
.falling-text div:nth-child(1) span:nth-child(6) {
  animation-delay: 0.6s;
}
.falling-text div:nth-child(2) span:nth-child(1) {
  animation-delay: 0.7s;
}
.falling-text div:nth-child(2) span:nth-child(2) {
  animation-delay: 0.8s;
}
.falling-text div:nth-child(2) span:nth-child(3) {
  animation-delay: 0.9s;
}
.falling-text div:nth-child(2) span:nth-child(4) {
  animation-delay: 1s;
}
.falling-text div:nth-child(2) span:nth-child(5) {
  animation-delay: 1.1s;
}
.falling-text div:nth-child(2) span:nth-child(6) {
  animation-delay: 1.2s;
}
.falling-text div:nth-child(2) span:nth-child(7) {
  animation-delay: 1.3s;
}
.falling-text div:nth-child(2) span:nth-child(8) {
  animation-delay: 1.4s;
}
</style>
