<template>
  <div class="container-fluid">
    <div class="container">
      <!-- NAVBAR -->
      <nav>
        <div class="logo">
          <img id="dark-logo" src="../assets/img/dark-logo.png" alt="" />
        </div>
        <div class="nav-links">
          <ul class="nav-ul">
            <li v-for="(el, i) in navLinks" :key="i">
              {{ el }}
            </li>
          </ul>
        </div>
        <div class="social-links">
          <ul class="social-ul">
            <li v-for="(el, i) in socialIcons" :key="i">
              <img :src="el.img" />
            </li>
          </ul>
        </div>
      </nav>
      <!-- HERO -->
      <div class="hero">
        <div class="hero-text">
          <h5>i'm wingman</h5>
          <h1>
            Peace On Earth <br />
            A Wonderful Wish <br />
            But No Way
          </h1>
          <p>
            Succes isn't overnight. It's when everyday you get a little <br />
            better than the day before. It all adds up.
          </p>
          <button class="btn">Get Started For Free &#8594;</button>
        </div>

        <div class="hero-img">
          <img src="../assets/img/home-movation-hero-image.png" alt="" />
        </div>
      </div>
    </div>

    <!-- NAV-LATERALE -->

    <div class="side-bar">
      <div class="sidebar-icon">
        <img src="../assets/icons/school-triangle-svgrepo-com.svg" alt="" />
      </div>
      <div class="sidebar-icon">
        <img src="../assets/icons/circle-my-custom-svg.svg" alt="">
      </div>
      <div class="sidebar-icon">
        <img src="../assets/icons/book-solid.svg" alt="">
      </div>
      <div class="sidebar-icon">
        <img src="../assets/icons/cart-shopping-solid.svg" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderHero",
  data() {
    return {
      navLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
      socialIcons: [
        { img: require(`../assets/icons/twitter-brands.svg`) },
        { img: require(`../assets/icons/facebook-f-brands.svg`) },
        { img: require(`../assets/icons/instagram-brands.svg`) },
        { img: require(`../assets/icons/linkedin-brands.svg`) },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixin.scss";

.container {
  display: flex;
  flex-wrap: wrap;
  row-gap: 25px;
}

.container-fluid {
  min-height: 525px;
  background-color: $bg-hero;
  background-image: url("../assets/img/background-pattern-wavify.png");
  position: relative;
}

//NAV//

nav {
  min-height: 52px;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

.logo,
.social-links {
  width: 110px;
  display: flex;
  align-items: center;
}

.nav-links {
  flex-grow: 1;
}
#dark-logo {
  width: 100%;
}

.nav-ul {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  font-family: $normal-text;
  font-size: 10px;
  flex-wrap: wrap;
  margin: 0 40px;

  & li {
    cursor: pointer;
    font-weight: 600;
    color: $nav-text;
    display: flex;
    align-items: center;
    gap: 5px;

    &::after {
      content: url("../assets/icons/chevron-down-solid.svg");
      width: 7px;
      filter: invert(24%) sepia(33%) saturate(682%) hue-rotate(207deg)
        brightness(94%) contrast(92%);
    }
  }
}

.social-ul {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 15px;

  & li {
    height: 14px;
    cursor: pointer;

    & img {
      height: 100%;
      filter: invert(24%) sepia(51%) saturate(0%) hue-rotate(276deg)
        brightness(88%) contrast(111%);
    }
  }
}

//HERO//

.hero {
  display: flex;
  flex-wrap: wrap;
  min-height: 450px;
  width: 100%;
}

.hero-text,
.hero-img {
  height: 100%;
  width: 50%;
  flex-grow: 1;
}

.hero-text {
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

.hero-img {
  background-image: url("../assets/img/home-movation-shape-face.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: bottom right;
  position: relative;

  & img {
    height: auto;
    width: 88%;
    position: absolute;
    bottom: 0;
  }
}

.side-bar {
  position: absolute;
  top: 50%;
  right: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 14px;
  background-color: white;
  padding: 15px 2px;
  border-radius: 5px;
  box-shadow: -7px 0px 15px -2px rgba(0, 0, 0, 0.48);
  transform: translateY(-50%);

  & .sidebar-icon {
    height: 15px;
    width: 22px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;

    & img {
      height: 100%;
    }
  }
}
</style>
