<!--// 父组件-->
<template>
  <div id="app">
    <app-header v-on:titleChanged="updateTitle" ></app-header>
    <!--//与子组件titleChanged自定义事件保持一致-->
    <h2>{{title}}</h2>
    <!--// updateTitle($event)接受传递过来的文字-->
  </div>
</template>
<script>
  import Header from "./components/Users"
  export default {
    name: 'App',
    data(){
      return{ title:"这是---父组件原先的值"  }
    },
    methods:{
      updateTitle(e){  this.title = e; }
    },
    components:{  "app-header":Header, }
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
