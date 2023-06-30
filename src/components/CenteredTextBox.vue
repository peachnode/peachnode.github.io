<template>
  <div class="centered-text-box">
    <p v-html="text"></p>
  </div>
</template>

<script>
export default {
  name: "CenteredTextBox",
  props: {
    text: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.centered-text-box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 60%;
  height: 80%;
  padding: 0;
  font-size: 35px;
  text-align: left;
  overflow: hidden;
  transition: max-width 0.5s;
}

@media screen and (max-width: 1000px) {
  .centered-text-box {
    font-size: 99%;
  }
}
</style>
