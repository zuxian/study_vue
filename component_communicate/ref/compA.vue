<template><h1>我是子组件： {{msg}}</h1></template>
<script>
  export default {
    name: "compA",
    data () { return { title: '子子子的title',  msg:'子子子的msg'} },
    methods: {
      sayHello () { window.alert('Hello'); },
      emitEvent(msg){ this.msg=msg; }
    }
  }
</script>

<style scoped>

</style>