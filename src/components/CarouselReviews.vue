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
                        review:"",
                        img:"",
                        author:"",
                        job:"",
                        active: true,
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