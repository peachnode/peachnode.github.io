<template>
  <div class="home">
    <div class="container">
      <img
        alt="peach hub logo"
        src="../assets/logo-transparent.png"
        class="logo"
      />
      <HeadLine :msg="headLineMessage" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HeadLine from "@/components/HeadLine.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    HeadLine,
  },
  data() {
    return {
      headLineMessage: "WEBSITE COMING AUG 2023",
    };
  },
});
</script>

<style scoped>
.home {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  height: 100vh;
}

.container {
  width: 60vw;
  height: auto;
}

.logo {
  width: 40%; /* Set the maximum width of the logo to 100% of its container */
  height: auto; /* Allow the logo to scale proportionally */
  transition: max-width 0.5s;
  padding-top: 40px;
}

@media screen and (max-width: 600px) {
  .logo {
    width: 80%; /* Reduce the logo's max-width for smaller screens */
  }
}
@font-face {
  font-family: "Quantico";
  src: url("../fonts/Quantico/Quantico-Bold.ttf") format("truetype"),
    url("../fonts/Quantico/Quantico-BoldItalic.ttf") format("truetype"),
    url("../fonts/Quantico/Quantico-Italic.ttf") format("truetype"),
    url("../fonts/Quantico/Quantico-Regular.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}
</style>
