<template>
  <div class="container-fluid">
    <div class="container">
      <h6>begin your journey at maxcoach</h6>
      <h2>Latest <span>Online Courses</span></h2>

      <div class="card-wrapper">
        <div class="card" v-for="(el, i) in courses" :key="i">
          <div class="card-thumb">
            <img :src="el.img" alt="" />
          </div>

          <div class="card-text">
            <div class="card-price">
              {{ el.price }}
            </div>
            <div class="card-title">
              {{ el.title }}
            </div>
            <div class="card-description">
              <span>
                <img src="../assets/icons/file-lines-regular.svg" alt="" />
                {{ el.lessons }}</span
              >
              <span>
                <img src="../assets/icons/user-regular (1).svg" alt="" />
                {{ el.students }}</span
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoursesSection",
  data() {
    return {
      courses: [
        {
          img: require(`../assets/img/motivation-course-06-480x298.jpg`),
          price: "$30.00",
          title: "How to be Successful: Create A Growth Mindset For Success",
          lessons: "3 Lessons",
          students: "50 Students",
        },
        {
          img: require(`../assets/img/motivation-course-05-480x298.jpg`),
          price: "$30.00",
          title: "How to Build Confidence in Your Abilities",
          lessons: "1 Lesson",
          students: "50 Students",
        },
        {
          img: require(`../assets/img/motivation-course-04-480x298.jpg`),
          price: "$20.00",
          title: "Productivity Machine - Focus in a Distracted World",
          lessons: "5 Lessons",
          students: "50 Students",
        },
        {
          img: require(`../assets/img/motivation-course-03-480x298.jpg`),
          price: "$20.00",
          title: "Effective Time Management Mastery- Complete Guide",
          lessons: "18 Lessons",
          students: "50 Students",
        },
        {
          img: require(`../assets/img/motivation-course-02-480x298.jpg`),
          price: "$25.99",
          title: "Body Language Secrets for Entrepreneurs",
          lessons: "19 Lessons",
          students: "50 Students",
        },
        {
          img: require(`../assets/img/motivation-course-01-480x298.jpg`),
          price: "$19.99",
          title: "Management Skills: The Science of Leadership",
          lessons: "17 Lessons",
          students: "50 Students",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/mixin.scss";

.container {
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  & h6 {
    font-family: $small-caps;
    text-transform: uppercase;
    font-size: 10px;
    color: $grey-text;
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
}

.card-wrapper {
  margin-top: 40px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  width: 100%;
  row-gap: 45px;
  gap: 15px;

  & .card {
    min-height: 275px;
    width: 250px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    font-family: $normal-text;

    & .card-thumb {
      width: 100%;
      height: 152px;

      & img {
        width: 100%;
        height: 100%;
        border-radius: 3px;
      }
    }

    & .card-text{
        padding: 0 18px;
    }

    & .card-price {
      color: $green-text;
      padding: 12px 0;
      font-weight: 800;
      font-size: 14px;
    }

    & .card-title {
      color: $dark-text;
      font-weight: 600;
      font-size: 13px;
    }

    & .card-description {
        color: $grey-text;
        font-size: 8px;
        margin-top: 20px;
        display: flex;

        & span{
            padding-right: 15px;
            font-weight: 600;
            display: flex;

                & img{
                    height: 8px;
                    width: 8px;
                    margin-right: 5px;
                    filter: invert(79%) sepia(14%) saturate(5%) hue-rotate(116deg) brightness(82%) contrast(92%);
                }
            
        }
    }
  }
}
</style>
