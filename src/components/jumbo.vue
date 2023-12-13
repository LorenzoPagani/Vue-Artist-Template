<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "jumbo",
    data() {
        return {
            store,

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
    <div class="jumbo d-flex justify-content-center align-items-center">
        <div class="title-wrapper z-1 text-center">
            <h2 class="italic">Hello, I'm Matin</h2>
            <h2 class="fw-bold">Artist coaching and mentor might be for you</h2>
            <button class="btn main-btn">Get started today</button>
        </div>
        <img class="position-absolute  shape-1" src="../assets/images/artist-shape-01-300x288.png" alt="">
        <img class="position-absolute  shape-2" src="../assets/images/artist-shape-02-300x162.png" alt="">
        <img class="position-absolute  stain-1" src="../assets/images/stain.svg" alt="">
        <img class="position-absolute  stain-2" src="../assets/images/stain-2.svg" alt="">
        <img class="position-absolute  shape-3" src="../assets/images/artist-shape-03-201x300.png" alt="">
        <img class="position-absolute  shape-4" src="../assets/images/artist-shape-04-127x300.png" alt="">
        <img class="position-absolute  shape-5" src="../assets/images/artist-shape-05-300x198.png" alt="">
        <img class="position-absolute  shape-6" src="../assets/images/maxcoach-shape-12-100x100.png" alt="">
        <img class="position-absolute  shape-7" src="../assets/images/artist-hero-image-03.png" alt="">
        <img :style="{ left: 15.37 + store.mouseX + '%', top: 14.47 + store.mouseY + '%' }"
            class="position-absolute  shape-8" src="../assets/images/artist-hero-image-02-232x300.jpg" alt="">
        <img :style="{ left: 10 - store.mouseX + '%', top: 50 - store.mouseY + '%' }" class="position-absolute  shape-9"
            src="../assets/images/artist-hero-image-01.jpg" alt="">
        <img :style="{ left: 70 - store.mouseX + '%', top: 30 - store.mouseY + '%' }" class="position-absolute  shape-10"
            src="../assets/images/artist-hero-image-04.jpg" alt="">

    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

@mixin main-button {
    background-color: $mainBtn;
    color: white;

    &:hover {
        background-color: $hoveredMainBtn;

    }
}



.jumbo {
    height: 90vh;
    position: relative;
    background-color: #FBF9F6;


    .title-wrapper {
        width: 40%;
    }

    .italic {
        font-family: 'Rossela-Demo';
        color: $hoveredMainBtn;
        font-size: 3rem;
    }

    .main-btn {
        @include main-button()
    }

    .shape-1 {
        top: 0%;
        left: 54%;
        width: 40%;
    }

    .shape-2 {
        top: 0%;
        left: 0%;
        width: 45%;
    }

    .stain-1 {
        top: 58%;
        left: 0%;
        width: 15%;
    }

    .stain-2 {
        top: 80%;
        left: 66%;
        width: 6%;
    }

    .shape-3 {
        top: 8%;
        left: 0%;
        width: 25%;
    }

    .shape-4 {
        top: 15%;
        left: 85%;
        width: 10%;
    }

    .shape-5 {
        top: 63%;
        left: 74%;
        width: 23%;
    }

    .shape-6 {
        top: 70%;
        left: 70%;
        width: 12%;
    }

    .shape-7 {
        top: 50%;
        left: 25%;
        width: 14%;
    }

    .shape-8 {
        width: 16%;
        box-shadow: 7px 9px 15px 5px gray;
    }

    .shape-9 {
        width: 11%;
        box-shadow: 7px 9px 15px 5px gray;
    }

    .shape-10 {
        width: 20%;
        box-shadow: 7px 9px 15px 5px gray;
    }
}
</style>