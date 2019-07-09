<template>
  <div>
    <h1>{{ msg }}</h1>
  </div>
</template>
<script>
export default {
  data () {
    return {
      title: '我是標題'
    }
  },
  // props
  props: {
    msg: {
      type: String,
      default: '我是誰?'
    }
  }
}
</script>
<style>
</style>
