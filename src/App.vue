<template>
  <div id="app">
    <name/>
    <about/>
  </div>
</template>

<script>
import name from './components/Name.vue'
import about from './components/About.vue'

export default {
  name: 'app',
  components: {
    name,
    about
  }
}
</script>

<style>
</style>
