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
        <swiper :slidesPerView="3" :loop="true" :centeredSlides="true" :spaceBetween="30" :grabCursor="true" :pagination="{
            clickable: true,
        }" :modules="modules" class="mySwiper">
            <swiper-slide class="slide">Slide 1</swiper-slide>
            <swiper-slide>Slide 2</swiper-slide><swiper-slide>Slide 3</swiper-slide>
            <swiper-slide>Slide 4</swiper-slide>
        </swiper>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.mySwiper {
    height: 200px;

    .slide {
        height: 100%;
        color: blue;
    }
}
</style>