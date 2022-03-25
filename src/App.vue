<template>
  <div id="app">
    <HeaderHero />
    <AboutMe />
    <CoursesSection />
    <BookStore />
    <!-- carousel-reviews
         section-blog
         footer-info -->
  </div>
</template>

<script>
import HeaderHero from "./components/HeaderHero.vue";
import AboutMe from "./components/AboutMe.vue";
import CoursesSection from "./components/CoursesSection.vue";
import BookStore from "./components/BookStore.vue";

export default {
  name: "App",
  components: {
    HeaderHero,
    AboutMe,
    CoursesSection,
    BookStore,
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
.btn{
  background-color: $green-text;
  color: white;
  padding: 10px 30px;
  border: none;
  border-radius: 5px;
  font-size: 11px;
  font-family: $normal-text;
  font-weight: 700;
  cursor: pointer;

  &:hover{
    background-color: #3F3A64;
  }
}
.col-6{
  width: 50%;
}

</style>
