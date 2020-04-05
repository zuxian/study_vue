<template>
  <div class="World">
    <h1>这是World组件，这是接受到的参数：{{ number }}</h1>
  </div>
</template>
<script>
  import bus from '../bus'
  export default {
    name: "World",
    data () { return { number: 0 } },
    created () { bus.$on('getParam', param => { this.number = param }) },
    beforeDestroy () {  bus.$off('getParam') }
  }
</script>









<style scoped>

</style>