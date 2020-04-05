<template>
  <div class="APP">
    <h1>我是父组件：{{title}}</h1>
    <button @click="getMyEvent">点击父组件</button>
    <compA ref="comA"></compA></div>
</template>
<script>
  import compA from "./components/compA.vue";
  export default {
    name: 'APP',
    data () { return { title: '父父父的title', msg:'父父父的msg'} },
    mounted () {
      const comA = this.$refs.comA;
      this.title = this.$refs.comA.title;
      comA.sayHello();  // 弹窗
    },
    methods:{  getMyEvent(){this.$refs.comA.emitEvent(this.msg)}  },
    //调用子组件的方法，comA是上边ref起的名字，emitEvent是子组件的方法。
    components: { compA }
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
