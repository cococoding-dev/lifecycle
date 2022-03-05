<template>
  <div id="app">
    <button @click="changeResult">click</button>
    {{ result }}
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      result: 0,
    };
  },

  methods: {
    changeResult() {
      console.log("1. changeResult");
      this.result = 1;
    },
  },

  beforeCreate() {
    console.log("1. beforeCreate");
  },

  created() {
    console.log("2. created");
  },

  // DOM <- template loading /

  beforeMount() {
    console.log("3. beforeMount");
  },

  mounted() {
    console.log("4. mounted");
  },

  // template

  beforeUpdate() {
    console.log("beforeUpdate");
  },

  updated() {
    console.log("updated");
  },

  // template
  beforeDestroy() {
    console.log("beforeDestroy");
  },

  destroyed() {
    console.log("destroyed");
  },

  computed: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
