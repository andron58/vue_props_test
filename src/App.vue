<template>
  <div id="app">
    <pre>{{ myArray }}</pre>
    <SomeComponent :parent-array="[...myArray]" />
  </div>
</template>

<script>
import SomeComponent from "./components/SomeComponent.vue";

export default {
  name: "App",
  data() {
    return {
      myArray: [
        {
          name: "Name1",
          value: "Value1"
        },
        {
          name: "Name2",
          value: "Value2"
        }
      ]
    };
  },
  components: {
    SomeComponent
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
