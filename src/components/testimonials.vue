<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';



// import required modules
import { Pagination } from 'swiper/modules';
export default {
    name: "testimonials",
    components: {
        Swiper,
        SwiperSlide,
    },
    data() {
        return {
            store,
            modules: [Pagination],
        }
    },
    methods: {

    },
    mounted() {
        register(this); //per debuggare il componente da console

    }
}
</script>
<template>
    <div class="container text-center">
        <div class="title-wrapper">
            <h2 class="italic">Testimonials</h2>
            <h2 class="fw-bold mb-5">Why do people love me?</h2>
        </div>
        <swiper :slidesPerView="3" :loop="true" :centeredSlides="true" :spaceBetween="30" :grabCursor="true" :pagination="{
            clickable: true,
        }" :modules="modules" class="mySwiper">
            <swiper-slide class="slide">
                <h5 class="fw-bold">
                    High level of eficiency and
                    scientific teaching methods.
                </h5>
                <h5 class="mb-4">
                    I am free to learn at my own pace,
                    follow my own schedule and choose the
                    subject I want to learn from the
                    syllabus. Great study portal for people
                    like me.</h5>
                <img src="../assets/images/artist-testimonial-avatar-04.jpg" alt="">
                <div class="d-inline-block">
                    <p class="fw-bold">Mina hollace </p>
                    <p>/Freelancer</p>
                </div>
            </swiper-slide>

            <swiper-slide class="slide">
                <h5 class="fw-bold">
                    Professional team of specialists
                    and passionate mentors at reach

                </h5>
                <h5 class="mb-4">
                    I need to get a certification for English
                    proficiency and MaxCoach is my best
                    choice. Their tutors are smart and
                    professional when dealing with
                    students.</h5>
                <img src="../assets/images/artist-testimonial-avatar-01.jpg" alt="">
                <div class="d-inline-block">
                    <p class="fw-bold">Madley Pondor </p>
                    <p>/IT Specialist</p>
                </div>
            </swiper-slide>

            <swiper-slide class="slide">
                <h5 class="fw-bold">
                    The MaxCoach team works really
                    hard to ensure high quality

                </h5>
                <h5 class="mb-4">
                    I am happy with their arrangernent of
                    lessons and subjects. They reflect a
                    scientific investigation into effective
                    methods to be adopted for everyone.</h5>
                <img src="../assets/images/artist-testimonial-avatar-03.jpg" alt="">
                <div class="d-inline-block">
                    <p class="fw-bold">Luvic Dubble </p>
                    <p>/Private Tutor</p>
                </div>
            </swiper-slide>

            <swiper-slide class="slide">
                <h5 class="fw-bold">
                    lt's a choice of quality for people
                    with special needs

                </h5>
                <h5 class="mb-4">
                    I'm a very strict person so I require
                    everything to be organized and neat.
                    Then, l'Il be able to make things right
                    and shine. MaxCoach guys just got me.
                </h5>
                <img src="../assets/images/artist-testimonial-avatar-02.jpg" alt="">
                <div class="d-inline-block">
                    <p class="fw-bold">Draco Malfoy</p>
                    <p>/ Slytherin admin</p>
                </div>
            </swiper-slide>

        </swiper>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.title-wrapper {
    width: 47%;
    margin: auto;
}

.italic {
    font-family: 'Rossela-demo';
    font-size: 3rem;
    color: $hoveredMainBtn;
}

.mySwiper {


    .slide {
        height: 413px;
        width: 429px;
        border: 1px solid gray;
        border-radius: 10px;
        padding: 3rem;
        margin-bottom: 3rem;
        text-align: left;

        img {
            width: 40%;
            border-radius: 50%;
            margin-right: 2rem;
        }
    }
}
</style>