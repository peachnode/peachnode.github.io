<template>
  <div id="app">
    <div class="background"></div>
    <div class="content"></div>
    <nav v-if="showNavigationBar">
      <router-link to="/">home</router-link
      >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      <router-link to="/about">about</router-link>
    </nav>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      showNavigationBar: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Quantico, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-size: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
}

nav {
  padding: 30px;
  z-index: 1;
}

nav a {
  font-weight: bold;
  color: #ff886c;
  font-size: 30px;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #668d63;
}

.background {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-size: cover;
  background-position: center;
  opacity: 1; /* Adjust the opacity of the background image if desired */
  z-index: -1; /* Push the background behind the content */
  background-image: url("./assets/background.png");
}

.content {
  flex-grow: 1;
}
</style>
