<template>
  <header class="head-cont">
      <div class="logo">
        <img src="../assets/img/spotify-logo.png" alt="Logo Spotify">
      </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
.head-cont {
    background-color: $mainColor;
    padding: .3125rem;
    img {
        height: 2.5rem;
    }
 
}
</style>
