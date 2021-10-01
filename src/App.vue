<template>
  <div id="app"> 
    <Header />
    <main>
      <Albums>

      </Albums>
    </main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Albums from "./components/Albums.vue";
// import Icons from "./components/Icons.vue";
// import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Albums,
    // Icons,
    // Footer,
},
}
</script>

<style lang="scss">
@import "./assets/style/common.scss";
</style>

