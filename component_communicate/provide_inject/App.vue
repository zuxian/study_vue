<template>
  <div class="APP"><h1>我是祖父组件</h1><father-dom></father-dom></div>
</template>
<script>
  import fatherDom from "./components/fatherDom.vue";
  export default {
    name: 'APP',
    provide: { fooNew: "传给孙子组件的值" },
    data () { return { } },
    components: { fatherDom }
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
