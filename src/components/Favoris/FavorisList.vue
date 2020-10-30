<template>
  <div class="container w-4/5 mx-auto mt-4">
    <h1 class="font-bold text-xl mb-2" style="text-align: center">
      Mes tournois en favoris
    </h1>

    <div v-if="favoris.length === 0">
      <p>pas de favoris</p>
    </div>
    <div v-else>
      <div class="favoriscard">
        <favoris-card
          v-for="tournoi in favoris"
          :key="tournoi.nom"
          :tournoi="tournoi"
        >
        </favoris-card>
      </div>
    </div>
  </div>
</template>

<script>
import FavorisCard from "./FavorisCard.vue";
export default {
  name: "favoris-list",
  props: ["favoris"],
  components: {
    FavorisCard,
  },
};
</script>

<style scoped>
.favoriscard {
  display: block;
  margin-left: 35%;
  margin-top: 10%;
}
</style>
