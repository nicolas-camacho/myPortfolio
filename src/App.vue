<template>
  <div id="app">
    <div class="tabs is-centered">
      <ul>
        <li :class="{ 'is-active': displayName }" @click="showName()"><a>Home</a></li>
        <li :class="{ 'is-active': displayAbout }" @click="showAbout()"><a>About</a></li>
        <li :class="{ 'is-active': displayWorks }" @click="showWorks()"><a>Repositories</a></li>
      </ul>
    </div>
    <name v-if="displayName"/>
    <about v-if="displayAbout"/>
    <works v-if="displayWorks"/>
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
  },
  data(){
    return{
      displayName: true,
      displayAbout: false,
      displayWorks: false
    }
  },
  methods: {
    showName() {
      this.displayName = true
      this.displayAbout = false
      this.displayWorks = false
    },
    showAbout() {
      this.displayAbout = true
      this.displayName = false
      this.displayWorks = false
    },
    showWorks() {
      this.displayWorks = true
      this.displayName = false
      this.displayAbout = false
    }
  }
}
</script>

<style scope>
  .tabs{
    margin-bottom: 0 !important;
  }

  a{
    font-weight: bold;
  }
</style>
