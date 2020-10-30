<template>
  <div class="bg-blue-500 p-5 text-center font-bold">
    <a
      v-for="(link, index) in navigation"
      :key="index"
      href="#"
      @click="selectComponent(link.component)"
      class="m-5 p-5 hover:text-white "
    >
      {{ link.name }}
    </a>
  </div>
</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      navigation: [
        { name: "Les tournois", component: "tournoi-list" },
        { name: "Mes tournois favoris", component: "favoris-list" },
      ],
    };
  },
  methods: {
    selectComponent(comp) {
      this.$emit("change-component", comp);
    },
  },
};
</script>

<style></style>
