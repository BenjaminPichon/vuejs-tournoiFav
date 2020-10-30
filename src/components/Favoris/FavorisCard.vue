<template>
  <div v-if="tournoi.status === 'soon'">
    <div
      class="w-1/2 rounded overflow-hidden shadow-lg border border-gray-400 m-1 bg-blue-500"
    >
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">{{ tournoi.nom }}</div>
        <p class="text-gray-700 text-base">
          {{ tournoi.description }}
        </p>
        <p>Jeu : {{ tournoi.jeu }}</p>
      </div>
    </div>
  </div>
  <div v-else-if="tournoi.status === 'happening'">
    <div
      class="w-1/2 rounded overflow-hidden shadow-lg border border-gray-400 m-1 bg-green-500"
    >
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">{{ tournoi.nom }}</div>
        <p class="text-gray-700 text-base">
          {{ tournoi.description }}
        </p>
        <p>Jeu : {{ tournoi.jeu }}</p>
      </div>
    </div>
  </div>
  <div v-else>
    <div
      class="w-1/2 rounded overflow-hidden shadow-lg border border-gray-400 m-1 bg-red-500"
    >
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">{{ tournoi.nom }}</div>
        <p class="text-gray-700 text-base">
          {{ tournoi.description }}
        </p>
        <p>Jeu : {{ tournoi.jeu }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "favoris-card",
  props: ["tournoi"],
};
</script>

<style></style>
