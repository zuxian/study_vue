<template>
  <div class="child-2">
    <p>in child2:</p> <p>接受到的值 props: {{pChild2a}}---- {{pChild2b}}  </p>
    <p>传递下去的值 $attrs: {{$attrs}}</p> <hr>
  </div>
</template>
<script>
  export default {
    props:  { pChild2a: String ,  pChild2b: String  },
    data () { return {};  },
    inheritAttrs: false,
    mounted () {  this.$emit('test2', '我是孙孙孙'); }
  };
</script>

<style scoped>

</style>