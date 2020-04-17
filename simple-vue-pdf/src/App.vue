<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <Pdfpage /> -->
    <pdf-demo />
    <!-- <MorePage>更多页面</MorePage> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <pdfshow></pdfshow> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Pdfpage from './components/pdfpage'
// import MorePage from './components/MorePage'
// import pdfshow from './components/Pdfshow'
import pdfDemo from './components/demopdf'

export default {
  name: 'App',
  components: {
    // pdfshow,
    // Pdfpage,
    pdfDemo
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
