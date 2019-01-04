<template>
  <div class="app">
    <img width="25%" src="./assets/logo.png" /> <StudyVue />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld";
import StudyVue from "./components/StudyVue";

export default {
  // name: "App",
  components: {
    //     HelloWorld,
    StudyVue
  }
};
</script>

<style>
.app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
