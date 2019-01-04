<template>
  <div class="study_wrap">
    <!--
        6<h1>Vue is Good</h1>
      <p>{{ user.lastName }} {{ user.firstName }}</p>
    -->
    <h2 v-show="toggle">Hello</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggle: true,
      colors: ["red", "green", "blue"],
      user: {
        lastName: "Yamada",
        firstName: "Takashi"
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
