<template>
  <div class="home">
    <div class="container">
      <img
        alt="peach hub logo"
        src="../assets/logo-transparent.png"
        class="logo"
      />
      <HeadLine msg="Welcome to our website" />
    </div>
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
</style>
