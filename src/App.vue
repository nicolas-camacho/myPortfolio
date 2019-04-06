<template>
  <div id="app">
    <name/>
    <about/>
    <works/>
  </div>
</template>

<script>
import name from './components/Name.vue'
import about from './components/About.vue'
import works from './components/Works.vue'

export default {
  name: 'app',
  components: {
    name,
    about,
    works
  }
}
</script>

<style>
</style>
