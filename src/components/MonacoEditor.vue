<template>
  <div>
    <h3 class="">Wellcome to VUE MONACO EDITOR demo</h3>
    <div class="monaco-box" id="monacoContainer"></div>
  </div>
</template>

<script>
  import * as monaco from 'monaco-editor'
  export default {
    data () {
      return {
        options: {
          language: 'javascript',
          value: '',
          fontSize: '14',
        },
        editor: null,
      }
    },
    mounted () {
      monaco.editor.setTheme('vs-dark')
      this.editor = monaco.editor.create(
        document.getElementById('monacoContainer'),  //  页面里的 DOM 元素
        this.options,  // 各种配置
      )
    }
  }
</script>

<style>
  .monaco-box {
    width: 680px;
    height: 400px;
    margin: 0 auto;
    border: 1px solid #ccc;
  }
</style>