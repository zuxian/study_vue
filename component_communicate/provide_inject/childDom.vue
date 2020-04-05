<template>
  <div> <h1>fooNew：{{fooNew}}</h1> </div>
</template>
<script>
  export default {
    name: "childDom",
    inject: ["fooNew"],
    methods: {}
  };
</script>

<style scoped>

</style>