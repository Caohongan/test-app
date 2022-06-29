<template>
  <div id="app">
    <OutProject />
    <ContactUs/>
  </div>
</template>

<script>

import OutProject from './components/OurProject.vue'
import ContactUs from './components/ContactUs.vue'
export default {
  name: 'App',
  components: {
    OutProject,
    ContactUs
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 0 200px;
}
</style>
