<!--//App.vue父组件-->
<template>
  <div id="app">
    <!--//users="users" 前者自定义名称便于子组件调用，后者要传递数据名-->
    <users v-bind:users="users"></users>
  </div>
</template>
<script>
  import Users from "./components/Users"
  export default {
    name: 'App',
    data(){
      return{  users:["Henry","Bucky","Emily"]  }
    },
    components:{  "users":Users  }
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
