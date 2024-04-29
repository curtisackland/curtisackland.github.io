<script>
export default {
  name: "ContactView",
};
</script>

<template>
  <div class="contact-me-container">
    <h1 class="contact-me-header">Contact Me</h1>
    <p style="text-align: center">
      Feel free to email me or message me on LinkedIn!
    </p>
    <div
      style="
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-content: center;
        align-items: center;
      "
    >
      <button class="contact-me-button link-icons">
        <a class="mail-to-link" href="mailto: curtisackland@rogers.com">
          Email Me!
        </a>
      </button>
      <h2 style="margin: 8px">OR</h2>
      <a href="https://www.linkedin.com/in/curtis-ackland/" target="_blank">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          class="link-icons"
        >
          <path
            d="M20.5 2h-17A1.5 1.5 0 002 3.5v17A1.5 1.5 0 003.5 22h17a1.5 1.5 0 001.5-1.5v-17A1.5 1.5 0 0020.5 2zM8 19H5v-9h3zM6.5 8.25A1.75 1.75 0 118.3 6.5a1.78 1.78 0 01-1.8 1.75zM19 19h-3v-4.74c0-1.42-.6-1.93-1.38-1.93A1.74 1.74 0 0013 14.19a.66.66 0 000 .14V19h-3v-9h2.9v1.3a3.11 3.11 0 012.7-1.4c1.55 0 3.36.86 3.36 3.66z"
          ></path>
        </svg>
      </a>
    </div>
  </div>
</template>

<style scoped lang="scss">
.contact-me-container {
  white-space: normal;
  justify-content: center;
  padding: 2% 25% 0 25%;
}

@media (max-width: 1250px) {
  .contact-me-container {
    padding: 5% 5% 0 5%;
  }
}

.contact-me-header {
  white-space: normal;
  justify-content: center;
  text-align: center;
  margin-bottom: 12px;
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
  text-decoration: none;
  text-align: center;
  color: $accentColor;
}

.link-icons {
  fill: $baseFontColor;
  height: 60px;
  width: auto;
  margin: 4px 4px 4px 4px;
}
</style>
