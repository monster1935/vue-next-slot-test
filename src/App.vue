<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <test-slot>
    <hello-world v-if="isShow" msg="Welcome to Your Vue.js App"/>
  </test-slot>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TestSlot from './components/TestSlot.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TestSlot
  },
  data () {
    return {
      isShow: false
    }
  },
  mounted () {
    setTimeout(() => {
      this.isShow = true
    }, 2000)
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
