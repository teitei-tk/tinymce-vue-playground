<script setup>
import { onMounted, defineComponent } from "vue";

import tinymce from "tinymce/tinymce";

import "./styles/themes/sliver/theme";
import "./styles/icons/default/default/icons";
import "./styles/skins/ui/oxide/content.min.css";
import "./styles/skins/ui/oxide/skin.min.css";

import "tinymce/plugins/media";

// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Editor from "@tinymce/tinymce-vue";

const config = {
  plugins: ["media"],
  toolbar: "media",
  height: 400,
};

onMounted(() => {
  tinymce.init({
    selector: "textarea#hoge",
    plugins: ["media"],
    toolbar: "media",
  });
});
</script>

<template>
  <editor :init="config" />
  <textarea id="hoge"></textarea>
</template>

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
