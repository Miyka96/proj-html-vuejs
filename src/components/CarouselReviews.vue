<template>
    <div class="container-fluid">
        
        <div class="carousel-description">
            
        </div>

        <div class="carousel-img"></div>

        <div class="button">
            
        </div>
    </div>
</template>

<script>
    export default {
        name:"CarouselReviews",
        data(){
            return{
                carousel:[
                    {
                        review:"I am free to learn at my own pace ,follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me",
                        img: require(`../assets/img/testimonial-avata-02.jpg`),
                        author:"Mina Hollace",
                        job:"/Freelancer",
                    },
                                        {
                        review:"I learned what expected to learn from this course. I love the presenters and the manner of delivery. Resources abound too. I'm purchasing this course. I hope to meet you, guys in persons. Thank you.",
                        img: require(`../assets/img/testimonial-avata-01.jpg`),
                        author:"Tom Anderson",
                        job:"/Engineer",
                    },
                                        {
                        review:"This course was designed with extremely outstanding qualities. The keen devotion of all the professors are highly appreciated. You have made it possible for me to move on in my professional career. ",
                        img: require(`../assets/img/testimonial-avata-03.jpg`),
                        author:"Patrick Weasle",
                        job:"/Waiter",
                    },
                                        {
                        review:"This course was very well structured; videos were short and to the point, while being informative and interesting to listen to. Thank you very much!",
                        img: require(`../assets/img/testimonial-avata-04.jpg`),
                        author:"Bill Craig",
                        job:"/Freelancer",
                    },
                ],
            }
        },
    }
</script>

<style lang="scss" scoped>

@import "../assets/scss/mixin.scss";

    .container-fluid{
        display: flex;
        height: 465px;
        position: relative;
        margin-bottom: 40px;
    }
    .carousel-description, .carousel-img{
        width: 50%;
        height: 100%;
    }
    .carousel-img{
        background-image: url("../assets/img/home-movation-testimonial-image-768x562.jpg");
        background-size: cover;
        background-repeat: no-repeat;
    }
    .carousel-description{
        background-image: url("../assets/img/background-pattern-wavify.png");
        background-color: $bg-hero;
    }
</style>