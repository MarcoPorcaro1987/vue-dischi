<template>
  <div id="app">
    <Header @selectGenres="selectGenres" />
    <Albums :selectedGenre="selectedGenre">
      <Album />
    </Albums>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Albums from "./components/Albums.vue";
import Album from "./components/Albums.vue";

export default {
  name: "App",
  components: {
    Header,
    Albums,
    Album,
  },
  data() {
    return {
      selectedGenre: "",
    };
  },
  methods: {
    selectGenres(selectedGenre) {
      this.selectedGenre = selectedGenre;
    },
  },
};
</script>

<style lang="scss">
@import "./assets/style/common.scss";
</style>
