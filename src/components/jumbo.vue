<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "jumbo",
    data() {
        return {
            store
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
            <h2>Artist coaching and mentor might be for you</h2>
            <button class="btn main-btn">Get started today</button>
        </div>
        <img class="position-absolute z-0 shape-1" src="../assets/images/artist-shape-01-300x288.png" alt="">
        <img class="position-absolute z-0 shape-2" src="../assets/images/artist-shape-02-300x162.png" alt="">
        <img class="position-absolute z-0 shape-3" src="../assets/images/artist-shape-03-201x300.png" alt="">
        <img class="position-absolute z-0 shape-4" src="../assets/images/artist-shape-04-127x300.png" alt="">
        <img class="position-absolute z-0 shape-5" src="../assets/images/artist-shape-05-300x198.png" alt="">
        <img class="position-absolute z-0 shape-6" src="../assets/images/maxcoach-shape-12-100x100.png" alt="">
        <img class="position-absolute z-0 shape-7" src="../assets/images/artist-hero-image-03.png" alt="">
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500&display=swap');

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


    .title-wrapper {
        width: 40%;
    }

    .italic {
        font-family: 'Dancing Script', cursive;
        color: $hoveredMainBtn;
    }

    .main-btn {
        @include main-button()
    }

    .shape-1 {
        top: 1%;
        left: 42%;
        width: 52%;
    }

    .shape-2 {
        top: 0%;
        left: 0%;
        width: 45%;
    }

    .shape-3 {
        top: 14%;
        left: 0%;
        width: 25%;
    }

    .shape-4 {
        top: 15%;
        left: 85%;
        width: 10%;
    }

    .shape-5 {
        top: 71%;
        left: 74%;
        width: 23%;
    }

    .shape-6 {
        top: 73%;
        left: 70%;
        width: 12%;
    }

    .shape-7 {
        top: 52%;
        left: 25%;
        width: 14%;
    }
}
</style>