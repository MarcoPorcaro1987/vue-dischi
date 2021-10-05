<template>
  <header class="head-cont">
    <div class="logo">
      <img src="../assets/img/spotify-logo.png" alt="Logo Spotify" />
    </div>
    <div>
      <select v-model="genre" @change="$emit('selectGenres', genre)">
        <option value="Scegli un genere" selected>Scegli un genere</option>
        <option value="Jazz">Jazz</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Metal">Metal</option>
      </select>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      genre: "",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
.head-cont {
  background-color: $mainColor;
  padding: 0.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  img {
    height: 2.5rem;
  }
}
</style>
