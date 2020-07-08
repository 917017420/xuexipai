<template>
  <div id="app">
    <div id="nav">
      <Home/>
    </div>
  </div>
</template>
<script>
// eslint-disable-next-line no-unused-vars
import Home from './views/Home'
export default {
  name: 'App',
  components: {
    Home
  }
}
</script>
<style lang="stylus">
#app
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
  margin-top 0
  width 100%
body
  margin 0
</style>
