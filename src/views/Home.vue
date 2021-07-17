<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
  </div>
  <div id="example1" class="demo">
    <p>Using mustaches: {{ rawHtml }}</p>
    <p>Using v-html directive: <span v-html="rawHtml"></span></p>
  </div>
  <div v-bind:id="dynamicId">dynamicId</div>
  <button :disabled="isButtonDisabled">Button</button>
  <div :id="'list-' + id">list-1</div>
  <a v-bind:[attributeName]="url">attributeName</a>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Home",
  data() {
    return {
      rawHtml: '<span style="color: red">This should be red.</span>',
      dynamicId: "ididid",
      isButtonDisabled: true,
      id: 1,
      attributeName: "href",
      url: "https://www.google.co.jp/",
    };
  },
});
</script>

<style lang="scss">
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}
</style>
