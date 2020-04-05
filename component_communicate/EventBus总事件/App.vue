<template>
  <div class="APP">
    <hello></hello>
    <h1>---------我是APP 组件 ------------</h1>
    <world></world>
  </div>
</template>
<script>
  import Hello from '@/components/Hello'
  import World from '@/components/World'
  export default {
    name: 'APP',
    data () { return { } },
    components: { Hello, World }
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
