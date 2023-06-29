<template>
  <div class="home">
    <img alt="peach hub logo" src="../assets/logo.png" class="logo" />
    <HeadLine msg="Welcome to our website" />
    <SubLine :msg="subLineMessage" />
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
.logo {
  width: 500px; /* Set the width of the logo */
  /*height: 100px; !* Set the height of the logo *!*/
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
