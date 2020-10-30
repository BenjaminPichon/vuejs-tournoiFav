<template>
  <div
    class="w-1/2 rounded overflow-hidden shadow-lg border border-gray-400 m-1"
  >
    <div class="px-6 py-4">
      <div class="font-bold text-xl mb-2">{{ tournoi.nom }}</div>
      <p class="text-gray-700 text-base">
        {{ tournoi.description }}
      </p>
    </div>
    <div class="px-6 pt-4 pb-2 boutton">
      <base-button
        text="Ajouter au favoris"
        class="m-5"
        @click="addToFavoris"
      ></base-button>
    </div>
  </div>
</template>

<script>
export default {
  name: "tournoi-card",
  props: ["tournoi"],
  methods: {
    addToFavoris() {
      this.$emit("add-favoris", this.tournoi);
    },
  },
};
</script>

<style></style>
