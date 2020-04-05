<template>
  <div class="hello">
    <h1>这是Hello组件，这是发送的参数：{{ number }}</h1>
    <button @click="sendParam()">Hello发送数据按钮</button>
  </div>
</template>
<script>
  import bus from '../bus'
  export default {
    name: "Hello",
    data () { return { number: 123 } },
    methods: { sendParam () {  bus.$emit('getParam', this.number) } }
  }
</script>









<style scoped>

</style>