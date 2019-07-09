<template>
  <div class="view">
    <h1>{{ title }}</h1>
  </div>
</template>
<script>
export default {
  name: 'List',
  data () {
    return {
      title: 'TodoList'
    }
  }
}
</script>
<style>
.view {
  width: 400px;
  border: 1px solid gray;
  margin: 20px auto;
}
</style>
