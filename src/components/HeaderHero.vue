<template>
<div class="container-fluid">
  <div class="container">
      <!-- NAVBAR -->
      <nav>
        <div class="logo">
          <img id="dark-logo" src="../assets/img/dark-logo.png" alt="">
        </div>
        <div class="nav-links">
          <ul class="nav-ul">
            <li v-for="(el, i) in navLinks" :key="i">
              {{el}}
            </li> 
          </ul>
        </div>
        <div class="social-links">
          <ul class="social-ul">
            <li v-for="(el, i) in socialIcons" :key="i">
              <img :src="el.img">
            </li>
          </ul>
        </div>
      </nav>
      <!-- HERO -->
      <div class="hero">
        <div class="hero-text">
        <h5>i'm wingman</h5>
        <h1>Peace On Earth <br/> A Wonderful Wish <br/> But No Way</h1>
        <p>Succes isn't overnight. It's when everyday you get a little <br/> better than the day before. It all adds up. </p>
        </div>
        <div class="hero-img">
        
        </div>
      </div>
  </div>
</div>


  
</template>

<script>
  export default {
    name: "HeaderHero",
    data() {
    return {
      navLinks: [
        "Home",
        "Pages",
        "Courses",
        "Features",
        "Blog",
        "Shop"
      ],
      socialIcons: [
        {img: require (`../assets/icons/twitter-brands.svg`)},
        {img: require (`../assets/icons/facebook-f-brands.svg`)},
        {img: require (`../assets/icons/instagram-brands.svg`)},
        {img: require (`../assets/icons/linkedin-brands.svg`)}
      ]
    };
  },
  }
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixin.scss";

.container{
  display: flex;
  flex-wrap: wrap;
  row-gap: 25px;
}

.container-fluid{
  min-height: 525px;
  background-color: $bg-hero;
  background-image: url("../assets/img/background-pattern-wavify.png");
}

//NAV//

nav{
  min-height: 52px;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.logo, .social-links{
  width: 110px;
  display: flex;
  align-items: center;
}

.nav-links{
  flex-grow: 1;
}
#dark-logo{
  width: 100%;
}

.nav-ul{
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  font-family: $normal-text;
  font-size: 10px;
  flex-wrap: wrap;
  margin: 0 40px;

  & li{
    cursor: pointer;
    font-weight: 600;
    color: $nav-text;
    display: flex;
    align-items: center;
    gap: 5px;

    &::after{
      content: url("../assets/icons/chevron-down-solid.svg");
      width: 7px;
      filter: invert(24%) sepia(33%) saturate(682%) hue-rotate(207deg) brightness(94%) contrast(92%);
    }
  }
}

.social-ul{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 15px;

  & li{
    height: 14px;
    cursor: pointer;

    & img{
      height: 100%;
      filter: invert(24%) sepia(51%) saturate(0%) hue-rotate(276deg) brightness(88%) contrast(111%);
    }
  }

}

//HERO//

.hero{
  display: flex;
  flex-wrap: wrap;
  min-height: 450px;
  width: 100%;
}

.hero-text, .hero-img {
  height: 100%;
  width: 50%;
  flex-grow: 1;
}

.hero-text{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  color: $dark-text;

  & h5 {
    font-family: $small-caps;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 22px;
  }
  & h1 {
    font-family: $elegant-title;
    font-size: 30px;
    margin-bottom: 22px;
  }
  & p {
    font-family: $normal-text;
    font-size: 12px;
    margin-bottom: 22px;
  }
}



</style>
