<template>
  <div id="app">
    <HeaderView :msg="title"></HeaderView>
    <img src="./assets/logo.png">
    <ListView></ListView>
  </div>
</template>

<script>
// 導入組件
import ListView from './components/List'
import HeaderView from './components/Header'

export default {
  name: 'App',
  components: {
    // 註冊組件
    ListView,
    HeaderView
  },
  data () {
    return {
      title: 'Vue入門學習'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
