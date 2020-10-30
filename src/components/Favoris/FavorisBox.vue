<template>
  <div v-if="favoris.length === 0">
    <p>pas de favoris</p>
  </div>
  <div v-else>
    Nombre de tournois favoris : {{ favoris.length }}
    <span v-if="nbrFavoris">favoris</span>
    <span v-else>favori</span>
  </div>
</template>

<script>
export default {
  name: "favoris-box",
  props: ["favoris"],
  computed: {
    nbrFavoris() {
      if (this.favoris.length > 1) {
        return true;
      }
      return false;
    },
  },
};
</script>

<style></style>
