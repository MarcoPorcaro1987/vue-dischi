<template>
  <div class="container albums-cont" >
       <div class="album-cont" v-for="(elm, index) in albums" :key="index">
            <Album :info="elm" />
      </div>
  </div>
</template>

<script>
import Album from "./Album.vue";
import axios from "axios";

export default {
    name: "Albums",
    components: {
        Album
  },
  data(){
      return {
          albums : []
      }
  },
  created(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) =>{
            this.albums = res.data.response;
        }
        );
  }
}
</script>

<style lang="scss" scoped>
.albums-cont{
    display: flex;
    flex-wrap: wrap;
    gap: .9375rem 1.5625rem;
    .album-cont{
        width: calc(100% / 5 - 1.5625rem);
    }
}
</style>