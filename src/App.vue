<template>
  <tournoi-list></tournoi-list>
  <favoris-list></favoris-list>
  <navbar></navbar>
  <participation-list></participation-list>
</template>

<script>
import TournoiList from './components/Tournoi/TournoiList.vue'
import FavorisList from './components/Favoris/FavorisList.vue'
import Navbar from './components/Navigation/Navbar.vue'
import ParticipationList from './components/Participation/ParticipationList.vue'

export default {
  name: 'App',
  components: {
    TournoiList,
    FavorisList,
    Navbar,
    ParticipationList
  }
}
</script>

<style>
</style>
