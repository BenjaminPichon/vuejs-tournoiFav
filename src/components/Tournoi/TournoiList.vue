<template>
  <h1 class="font-bold text-xl mb-2" style="text-align: center">
    Liste des tournois sur le site
  </h1>
  <favoris-box :favoris="favoris"></favoris-box>
  <div class="tournoicard">
    <tournoi-card
      v-for="(tournoi, index) in tournoisData.tournois"
      :key="index"
      :tournoi="tournoi"
      @add-favoris="addTournoiToFavoris"
      @add-participation="addTournoiToParticipation"
    >
    </tournoi-card>
  </div>
</template>

<script>
import tournoisData from "../../assets/data/tournois.json";
import TournoiCard from "./TournoiCard.vue";
import FavorisBox from "../Favoris/FavorisBox.vue";

export default {
  name: "tournois-list",
  components: {
    TournoiCard,
    FavorisBox,
  },

  data() {
    return {
      tournoisData: tournoisData,
      favoris: [],
    };
  },
  methods: {
    addTournoiToFavoris(tournoi) {
      this.favoris.push(tournoi);
      this.$emit("update-favoris", tournoi);
    },
  },
};
</script>

<style scoped>
.tournoicard {
  display: block;
  margin-left: 35%;
  margin-top: 10%;
}
</style>
