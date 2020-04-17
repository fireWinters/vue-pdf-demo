<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Pdfpage >这是PDF文件链接</Pdfpage>
    <MorePage>更多页面</MorePage>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Pdfpage from './components/pdfpage'
import MorePage from './components/MorePage'

export default {
  name: 'App',
  components: {
    Pdfpage,
    MorePage
  }
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
