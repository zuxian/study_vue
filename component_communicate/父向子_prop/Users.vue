<!--//users子组件-->
<template>
  <div class="hello">
    <ul>
      <li v-for="user in users">{{user}}</li>//父组件遍历传递过来的值，然后呈现到页面
    </ul>
  </div>
</template>
<script>
  export default {
    name: 'User',
    props:{
      users:{           //这个就是父组件中子标签自定义名字
        type:Array,
        required:true
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
