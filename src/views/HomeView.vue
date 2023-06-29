<template>
  <div class="home">
    <div class="container">
      <img
        alt="peach hub logo"
        src="../assets/logo-transparent.png"
        class="logo"
      />
      <HeadLine msg="Welcome to our website" />
      <SubLine :msg="subLineMessage" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HeadLine from "@/components/HeadLine.vue";
import SubLine from "@/components/SubLine.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    HeadLine,
    SubLine,
  },
  data() {
    return {
      subLineMessage:
        "Peach Hub ist ein Ort, an dem Studentinnen der Fakultät IV sich vernetzen und langfristige Beziehungen aufbauen können, uns gegenseitig unterstützen und uns zusammen für ein angenehmeres Klima für Studentinnen* an der Fakultät einsetzen.",
    };
  },
});
</script>

<style scoped>
.home {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.container {
  width: 30vw;
  height: auto;
  margin: 0 auto;
  padding: 20px;
}

.logo {
  width: 100%; /* Set the maximum width of the logo to 100% of its container */
  height: auto; /* Allow the logo to scale proportionally */
  /*transition: max-width 0.5s;*/
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
