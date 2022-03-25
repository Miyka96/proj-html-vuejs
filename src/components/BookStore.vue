<template>
  <div class="container-fluid">
    <section class="container">
      <div class="col-5">
        <h6>book store online</h6>
        <h2>
          Be Alpha With <br />
          <span>Wingman's Book</span>
        </h2>

        <ul>
          <li>Help you understand yourself better</li>
          <li>Revealing mature tips</li>
          <li>Give the right advice</li>
          <li>Fascinating example of alpha man</li>
        </ul>

        <button class="btn">Get Free Ebook</button>
      </div>

      <div class="col-7">
        <div class="col-6">
          <div class="card">
            <div class="card-thumb">
              <ul>
                <li>
                  <img src="../assets/icons/magnifying-glass-solid.svg" />
                </li>
                <li><img src="../assets/icons/cart-shopping-solid.svg" /></li>
                <li><img src="../assets/icons/heart-solid.svg" /></li>
                <li><img src="../assets/icons/signal-solid.svg" /></li>
              </ul>
            </div>
            <div class="card-description">
              <div class="card-title">Alpha man by Maxcoach</div>
              <div class="card-price">$29.00</div>
            </div>
          </div>
        </div>
        <div class="col-6">
          <div class="card">
            <div class="card-thumb2">
              <ul>
                <li>
                  <img src="../assets/icons/magnifying-glass-solid.svg" />
                </li>
                <li><img src="../assets/icons/cart-shopping-solid.svg" /></li>
                <li><img src="../assets/icons/heart-solid.svg" /></li>
                <li><img src="../assets/icons/signal-solid.svg" /></li>
              </ul>
            </div>
            <div class="card-description">
              <div class="card-title">Real man 4.0 by Maxcoach</div>
              <div class="card-price">$39.00</div>
            </div>
          </div>
        </div>
      </div>

      <ul class="logo-wrapper">
        <li class="logo-items" v-for="(el, i) in logo" :key="i">
          <img :src="el.img" />
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  name: "BookStore",
  data() {
    return {
      logo: [
        { img: require(`../assets/img/client-logo-05-primary.png`) },
        { img: require(`../assets/img/client-logo-06-primary.png`) },
        { img: require(`../assets/img/client-logo-07-primary.png`) },
        { img: require(`../assets/img/client-logo-04-primary.png`) },
        { img: require(`../assets/img/client-logo-03-primary.png`) },
        { img: require(`../assets/img/client-logo-02-primary.png`) },
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
  align-items: center;
  justify-content: flex-start;
  margin-top: 50px;

  .col-5 {
    width: 45%;

    & h6 {
      font-family: $small-caps;
      text-transform: uppercase;
      font-size: 10px;
      color: $dark-text;
      letter-spacing: 1px;
      margin-bottom: 10px;
    }
    & h2 {
      font-size: 28px;
      font-family: $elegant-title;
      color: $dark-text;
      & span {
        color: $green-text;
      }
    }

    ul {
      padding: 25px 0;
    }

    li {
      padding: 5px 0;
      font-family: $normal-text;
      font-size: 12px;
      color: $grey-text;
    }

    li:before {
      content: url("../assets/icons/check-mark.svg");
      display: inline-block;
      padding-right: 1em;
      height: auto;
      width: 10px;
    }

    .btn {
      margin-bottom: 20px;
    }
  }

  .col-7 {
    width: 55%;
    display: flex;
    gap: 10px;
    align-items: center;
  }

  .card {
    height: 280px;
  }
  .card-thumb {
    height: 215px;
    background-image: url("../assets/img/product-book-11-400x400.jpg");
    background-size: contain;
    background-repeat: no-repeat;
    display: flex;
    align-items: center;
    justify-content: flex-end;

    &:hover {
      li {
        opacity: 1;
      }
    }

    & ul {
      display: flex;
      flex-direction: column;
      padding-right: 20px;

      & li {
        background-color: white;
        border-radius: 50%;
        width: 25px;
        height: 25px;
        margin: 5px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        box-shadow: 0px 0px 14px 0px rgba(0, 0, 0, 0.15);
        opacity: 0;
        transition: opacity 0.5s ease-in-out;
        cursor: pointer;

        & img {
          width: 10px;
          filter: invert(16%) sepia(17%) saturate(8%) hue-rotate(333deg)
            brightness(95%) contrast(88%);
        }
      }
    }
  }
  .card-thumb2 {
    height: 215px;
    background-image: url("../assets/img/product-book-10-400x400.jpg");
    background-size: contain;
    background-repeat: no-repeat;
    display: flex;
    align-items: center;
    justify-content: flex-end;

    &:hover {
      li {
        opacity: 1;
      }
    }

    & ul {
      display: flex;
      flex-direction: column;
      padding-right: 20px;

      & li {
        background-color: white;
        border-radius: 50%;
        width: 25px;
        height: 25px;
        margin: 5px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        box-shadow: 0px 0px 14px 0px rgba(0, 0, 0, 0.15);
        opacity: 0;
        transition: opacity 0.5s ease-in-out;
        cursor: pointer;

        & img {
          width: 10px;
          filter: invert(16%) sepia(17%) saturate(8%) hue-rotate(333deg)
            brightness(95%) contrast(88%);
        }
      }
    }
  }

  .card-price {
    color: $green-text;
    padding: 12px 0;
    font-weight: 800;
    font-size: 13px;
  }

  .card-title {
    color: $dark-text;
    font-weight: 600;
    font-size: 11px;
  }

  .card-description {
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: $normal-text;
  }

  .logo-wrapper {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    margin-top: 45px;
    margin-bottom: 40px;

    .logo-items {
      width: 90px;
      max-height: 100px;

      & img {
        width: 100%;
        object-fit: contain;
        filter: invert(74%) sepia(5%) saturate(0%) hue-rotate(249deg) brightness(92%) contrast(81%);
        opacity: 0.3;
      }
    }
    .logo-items:last-child {
      width: 55px;
    }
  }
}
</style>
