<template>
  <div class="album">
      <img :src="info.poster" alt="info.title">
      <div class="title">{{info.title}} </div>
      <p class="author">{{info.author}}</p>
      <p class="year">{{info.year}}</p>
  </div>
</template>

<script>
export default {
  name: "Album",
  props:{ 
      info: Object
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables.scss";
    .album{
        background-color: $mainColor;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap:.625rem;
        height: 19rem;
        text-align: center;
        img{
            margin-top: 1.25rem;
            width: 7rem;
            height:7rem;
        }
        .title{
            color:white;
            font-weight: bold;
        }
        p{
            color: $textColor;
        }

    }
</style>
