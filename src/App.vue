<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <TopBar />
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import TopBar from './components/TopBar'

export default {
  name: 'App',
  components: {
    /* HelloWorld */
    TopBar
  }
}
</script>

<style>

</style>
