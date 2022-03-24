<template>
  <section class="container-fluid">
    <div class="container">

      <!-- statistiche -->
      <div class="statistics">
        <ul class="stat-ul">
          <li class="stat-li" v-for="(el, i) in statistics" :key="i">
            <div class="stat-num">{{ el.number }}</div>
            <div class="stat-title">{{ el.title }}</div>
          </li>
        </ul>
      </div>

      <!-- about-me -->
      <div class="about">
        <div class="col-6">
          <h4>about me</h4>
          <h1>
            How to Be an Alpha <br />
            Male: The 15 Habits of <br />
            True Alphas
          </h1>
        </div>
        <div class="col-6">
          <h3>
            Want to learn how to be <span>an alpha male</span>? How to be more masculine?
            How to be the man you've always wanted to be?
          </h3>
          <p>
            Your goal is to show the consistency of business, core values, and customer care.
            Punctuality, responsibility, individuality, accuracy, enthusiasm - you have to clearly
            explain how these qualities are applicable to your work. And the important thing is you do love what you do.
          </p>
        </div>
      </div>

      <!-- sezione con video -->
      <div class="video-section">
        <div class="col-7">
          <div class="video-wrapper">
              <img src="../assets/img/icon-youtube-play.png" alt="">
          </div>
        </div>

        <div class="col-5">
          <h3>
            "Every morning you have two choices: continue to sleep with 
            your dreams, or wake up and chase them."
          </h3>
          <img src="../assets/img/home-movation-shape-01.png" alt="">
          <h5>
            Kaixa Stark
          </h5>
          <p>
            wingman
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutMe",
  data() {
    return {
      statistics: [
        {
          number: "1926",
          title: "finished sessions",
        },
        {
          number: "100%",
          title: "satisfaction rate",
        },
        {
          number: "3092+",
          title: "enrolled learners",
        },
        {
          number: "200",
          title: "online instructors",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>

@import "../assets/scss/mixin.scss";

.stat-ul {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-top: 60px;
  margin-bottom: 60px;
}
.stat-li:not(:first-of-type) {
  background-image: url("../assets/img/background-pattern-grid-line-06.png");
}

.stat-li {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 5px;
  min-height: 65px;
  font-family: $small-caps;
  flex-grow: 1;

  & .stat-num {
    font-size: 21px;
    color: $green-text;
    font-weight: 600;
  }

  & .stat-title {
    font-size: 10px;
    letter-spacing: 1px;
    text-transform: uppercase;
    font-weight: 600;
    color: $dark-text;
  }
}

.about {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  flex-wrap: wrap;

  & .col-6{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    min-height: 168px;
    flex-wrap: wrap;
  }

  & h4 {
    font-family: $small-caps;
    text-transform: uppercase;
    font-size: 8px;
    letter-spacing: 1px;
    font-weight: 600;
    color: $green-text;
  }

  & h1 {
    font-family: $elegant-title;
    margin: 15px 0;
    color: $dark-text;
    font-size: 24px;
  }

  & h3{
    font-family: $normal-text;
    font-size: 12px;
    font-weight: 700;
    line-height: 20px;
    margin-bottom: 15px;
    margin-top: 20px;

    & span{
      color: $green-text;
      font-weight: 700;
    }
  }

  & p{
    font-family: $normal-text;
    color: $dark-text;
    font-size: 9px;
    line-height: 16px;
    font-weight: 500;
  }
}

.video-section{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  margin-top: 40px;

  & .col-7{
    width: 55%;

    & .video-wrapper{
      height: 280px;
      width: 100%;
      background-image: url("../assets/img/home-movation-video-poster-670x450.jpg");
      background-size: cover;
      display: flex;
      align-items: center;
      justify-content: center;

      & img{
        height: 46px;
        cursor: pointer;
      }
    }
  }

  & .col-5{
    width: 45%;
    padding: 0 50px;

    & h3{
      font-size: 16px;
      line-height: 30px ;
      color: $dark-text;
      font-family: $elegant-title;
      margin-bottom: 30px;
    }

    & h5{
      margin: 20px 0;
      font-size: 15px;
      font-family: $normal-text;
      font-weight: 800;
    }

    & p{
      text-transform: uppercase;
      font-family: $small-caps;
      font-size: 10px;
      color: $dark-text;
      letter-spacing: 0.5px;
      
    }
  }
}


</style>
