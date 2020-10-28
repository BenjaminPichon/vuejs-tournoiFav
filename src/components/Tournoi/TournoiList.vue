<template>
  <h1>Hello</h1>
  <div v-for="(tournoi,index) in tournoisData.tournois" :key="index">
      {{tournoi.nom}}
  </div>
</template>

<script>
import tournoisData from '../../assets/data/tournois.json'

export default {
    name: 'tournois-list',

    data() {
        return {
            tournoisData: tournoisData,
        }
    }
}
</script>

<style>

</style>