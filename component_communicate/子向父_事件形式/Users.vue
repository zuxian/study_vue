<!--// 子组件-->
<template>
  <header>
    <h1 @click="changeTitle">{{title}}</h1>
    <!--//绑定一个点击事件-->
  </header>
</template>
<script>
  export default {
    name: 'app-header',
    data() {
      return { title:"点击此处----即可实现子组件向父组件传值" }
    },
    methods:{
      changeTitle() {
        this.$emit("titleChanged","这是---子向父组件传递的值");//自定义事件  传递值“子向父组件传值”
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
