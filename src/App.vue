<template>
  <div id="app">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
export default {
  components: {
    Navbar
  }
}
</script>

<style lang="scss">
body {
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0;
  max-width: 90vw;
  min-height: 100vh;
}

#app {
  font-family: 'Roboto', sans-serif;
  margin-bottom: 100px;
  max-width: 90vw;
}
</style>
