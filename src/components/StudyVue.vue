<template>
  <div class="study_wrap">
    <!--
        <h1>Vue is Good</h1>
        <p>{{ user.lastName }} {{ user.firstName }}</p>
      <h2 v-show="toggle">Hello</h2>
    -->
    <ul>
      <li v-for="value in user">{{ value }}</li>
    </ul>

    <ul>
      <li v-for="(v, k) in user">{{ k }} : {{ v }}</li>
    </ul>

    <button v-on:click="onClick">Click</button>
    <p>{{ now }}</p>
    <!--
      <ul>
        <li v-for="color in colors">{{color }}</li>
      </ul>
    -->
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
        firstName: "Taro",
        age: 28
      },
      now: ""
    };
  },
  methods: {
    onClick: function() {
      // this.now = "XXX";
      this.now = new Date().toLocaleTimeString();
      alert();
    }
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
