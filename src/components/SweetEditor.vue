<template>
  <div class="sweet-editor-wrapper">
    <editor
      :value="value"
      @input="updateContent"
      :init="editorInit"
    />
  </div>
</template>

<script>
// Tinymce core
import tinymce from 'tinymce/tinymce'

// Tinymce assets
import 'tinymce/themes/silver/theme'
import 'tinymce/icons/default'

// Tinymce plugins
import 'tinymce/plugins/image'
import 'tinymce/plugins/link'
import 'tinymce/plugins/code'
import 'tinymce/plugins/table'
import 'tinymce/plugins/lists'
import 'tinymce/plugins/wordcount'

// Tinymce Vue Component Wrapper
import Editor from '@tinymce/tinymce-vue'

export default {
  name: 'SweetEditor',
  components: {
    Editor
  },
  props: {
    value: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      editorInit: {
        // required 
        // skin assets can be found in node_modules/tinymce/skins 
        // copy to public directory for script loading
        skin_url: `${process.env.VUE_APP_STATIC_BASE_PATH}tinymce/skins/ui/oxide`,

        plugins: ['image link code table lists wordcount'],
        height: 300
      }
    }
  },
  mounted() {
    tinymce.init({})
  },
  methods: {
    updateContent(content) {
      this.$emit('input', content)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
