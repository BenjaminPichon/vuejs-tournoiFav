<template>
  <navbar></navbar>
  <tournoi-list></tournoi-list>
  
</template>

<script>
import TournoiList from './components/Tournoi/TournoiList.vue'

import Navbar from './components/Navigation/Navbar.vue'

export default {
  name: 'App',
  components: {
    TournoiList,
    Navbar,
  }
}
</script>

<style>
</style>
