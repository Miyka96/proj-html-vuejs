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
      <div class="about"></div>
      <!-- sezione con video -->
      <div class="video-section"></div>
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

  & .stat-title{
    font-size: 10px;
    letter-spacing: 1px;
    text-transform: uppercase;
    font-weight: 600;
    color: $dark-text;
  }
}
</style>
