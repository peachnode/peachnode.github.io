<template>
  <div class="home">
    <img
      alt="peach hub logo"
      src="../assets/logo-transparent.png"
      class="logo"
    />
    <HeadLine msg="Welcome to our website" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HeadLine from "@/components/HeadLine.vue"; // @ is an alias to /src

export default defineComponent({
  name: "HomeView",
  components: {
    HeadLine,
  },
});
</script>

<style scoped>
.logo {
  width: 500px; /* Set the width of the logo */
  /*height: 100px; !* Set the height of the logo *!*/
}
</style>
