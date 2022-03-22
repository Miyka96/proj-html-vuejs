<template>
  <div id="app">
      <HeaderHero/>
    <!-- section-about-me
         section-courses
         section-book_store
         carousel-reviews
         section-blog
         footer-info -->
  </div>
</template>

<script>

import HeaderHero from "./components/HeaderHero.vue";
export default {
  name:"App",
  components: {
    HeaderHero,
  },

};

</script>

<style lang="scss">

@import "./assets/scss/mixin.scss";

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-weight: 400;
}
li{
  list-style: none;
}
a{
  text-decoration: none;
  color: currentColor;
}
img{
  display: block;
}
#app{
  width: 100%;
}
.container{
  width: 780px;
}
.container-fluid{
  width: 100%;
  display: flex;
  justify-content: center;
}

</style>
