<template>
  <div id="app"><child1 :p-child1a="child1a" :p-child1b="child1b"
               :p-child2a="child2a"    :p-child2b="child2b"  :p-childxxx="childxxx"
            v-on:test1="onTest1"  v-on:test2="onTest2"></child1></div>
          <!--//此处监听了两个事件，可以在B组件或者C组件中直接触发-->
</template>
<script>
  import Child1 from './components/Child1.vue';
  export default {
    name: 'APP',
    data () { return {
            child1a: "Javascript", child1b: "es6",
            child2a: "Html",  child2b: "CSS",  childxxx: "Vue"}; },
    components: { Child1 },
    methods: {
      onTest1 (msg) { console.log('我是祖父---'  + msg); },
      onTest2 (msg) { console.log('我是祖父---'   +  msg);  }
    }
  };
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
