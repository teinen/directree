<template>
  <div id="container">Hoge</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import * as monaco from "monaco-editor";
import IStandaloneCodeEditor = monaco.editor.IStandaloneCodeEditor;

@Component
export default class MonacoEditor extends Vue {
  private editor!: IStandaloneCodeEditor;

  mounted() {
    const container = <HTMLElement>document.getElementById("container");
    this.editor = monaco.editor.create(container, {
      value: "console.log('hogehoge');"
    });
    const model = monaco.editor.createModel("console.log('hogehoge');");
    this.editor.setModel(model);
  }
}
</script>

<style scoped lang="scss"></style>
