<template>
  <navbar @change-component="updateSelectedComponent"></navbar>

  <keep-alive>
    <component
      :is="selectedComponent"
      v-bind="currentProps"
      @update-favoris="updateSelection"
    >
    </component>
  </keep-alive>
</template>

<script>
import TournoiList from "./components/Tournoi/TournoiList.vue";
import FavorisList from "./components/Favoris/FavorisList.vue";

import Navbar from "./components/Navigation/Navbar.vue";

export default {
  name: "App",
  components: {
    TournoiList,
    FavorisList,
    Navbar,
  },
  data() {
    return {
      selectedComponent: "tournoi-list",
      favorisArray: [],
    };
  },
  computed: {
    currentProps() {
      if (this.selectedComponent == "favoris-list") {
        return { favoris: this.favorisArray };
      }
      return false;
    },
  },

  methods: {
    updateSelectedComponent(comp) {
      this.selectedComponent = comp;
    },
    updateSelection(tournoi) {
      this.favorisArray.push(tournoi);
    },
  },
};
</script>

<style></style>
