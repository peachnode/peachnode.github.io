<template>
  <div class="about">
    <CenteredTextBox :text="aboutText" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import CenteredTextBox from "@/components/CenteredTextBox.vue";

export default defineComponent({
  name: "AboutView",
  components: {
    CenteredTextBox,
  },
  data() {
    return {
      aboutText:
        "We are a group of women in tech at TU Berlin who come together to share knowledge, network and work on projects.<br/><br/>Our goal is to create a supportive network where women in tech can connect, learn and grow together. Our community is open to all women and non-binary (FLINTA) people at the TU interested in tech.",
    };
  },
});
</script>

<style>
.about {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80vh;
}
</style>
