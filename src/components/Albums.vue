<template>
  <main>
    <div class="container albums-cont">
      <div
        class="album-cont"
        v-for="(elm, index) in albumsFiltered"
        :key="index"
      >
        <Album :info="elm" />
      </div>
    </div>
  </main>
</template>

<script>
import Album from "./Album.vue";
import axios from "axios";

export default {
  name: "Albums",
  components: {
    Album,
  },
  props: ["selectedGenre"],
  data() {
    return {
      albums: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.albums = res.data.response;
      });
  },
  computed: {
    albumsFiltered() {
      const arrFiltered = this.albums.filter((elm) => {
        if (
          elm.genre.toLowerCase().includes(this.selectedGenre.toLowerCase())
        ) {
          return true;
        }
        return false;
      });
      return arrFiltered;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
.albums-cont {
  display: flex;
  flex-wrap: wrap;
  gap: 0.9375rem 1.5625rem;
  .album-cont {
    width: calc(100% / 5 - 1.5625rem);
  }
}
</style>
