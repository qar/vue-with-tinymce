<template>
  <div id="app">
    <sweet-editor v-model="content" />
  </div>
</template>

<script>
import SweetEditor from './components/SweetEditor.vue'

export default {
  name: 'App',
  components: {
    SweetEditor
  },
  data() {
    return {
      content: '<h1>A just work "Vue.js with tinymce but not Tinymce Cloud" demo</h1>'
    }
  },
}
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
