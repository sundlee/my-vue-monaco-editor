<template>
  <div id="app">
    <MonacoEditor
      width="800"
      height="500"
      theme="vs"
      language="javascript"
      :options="options"
      v-model="code"
      @change="onChange"
    ></MonacoEditor>
  </div>
</template>

<script>
import MonacoEditor from 'monaco-editor-vue-fixed';

export default {
  name: 'App',
  components: {
    MonacoEditor,
  },

  data() {
    return {
      code: 'const noop = () => {\nconsole.log(\'Hello World!\');\n};',
      options: {
        //Monaco Editor Options
      },
    };
  },
  methods: {
    onChange(value) {
      console.log(value);
    }
  },
}
</script>

<style>
.editor {
  width: 600px;
  height: 800px;
}
</style>
