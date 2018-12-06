<template>
  <div id="app">
    <h1>Directree</h1>
    <monaco-editor />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import MonacoEditor from "./components/MonacoEditor.vue";

export default Vue.extend({
  components: {
    MonacoEditor
  }
});
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
