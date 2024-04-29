<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "classFeatures",
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
    <div id="features" class="container">
        <img class="background-1" src="../assets/images/maxcoach-shape-03.png" alt="">
        <img class="background-2" src="../assets/images/stain-3.svg" alt="">
        <img class="background-3" src="../assets/images/artist-shape-01.png" alt="">
        <img class="background-4" src="../assets/images/maxcoach-shape-13.png" alt="">
        <div class="row justify-content-center align-items-center">
            <div class="col-12 text-center title-wrapper">
                <h2 class="italic">Artist Coaching</h2>
                <h3 class="fw-bold">I undestand what it takes to create. I can help you with</h3>
            </div>
        </div>
        <div class="row">
            <div class="col-md-6 col-12 card-wrapper">
                <div class="card align-self-start">
                    <img src="../assets/images/artist-box-image-01.png" alt="">
                    <h5>Online Courses</h5>
                    <p>Online art coaching now offers you a
                        very powerful way to redesign your
                        artist mind.</p>
                </div>
                <div class="card align-self-end">
                    <img src="../assets/images/artist-box-image-02.png" alt="">
                    <h5>One to One</h5>
                    <p>Getting the necessary clarity about the
                        current state to help you improve your
                        ability.</p>
                </div>
            </div>
            <div class="col-md-6 col-12 card-wrapper">

                <div class="card align-self-start">
                    <img src="../assets/images/artist-box-image-03.png" alt="">
                    <h5>Anywhere</h5>
                    <p>Access to valuable and portable
                        program which allow you to setup and
                        live anywhere want.</p>
                </div>
                <div class="card align-self-end">
                    <img src="../assets/images/artist-box-image-04.png" alt="">
                    <h5>On Time</h5>
                    <p>Punctuality is our top priority because
                        it's an essential criteria to assess a
                        program quality.</p>
                </div>
            </div>
        </div>
        <div class="row pt-5">
            <div class="col-5  text-center">
                <img class="mb-3" src="../assets/images/artist-quote-icon.png" alt="">

            </div>
            <div class="col-5"></div>
            <div class="col-5 text-center">
                <h2 class="bold">I coach and mentor
                    visual artists, like
                    you, to Create Like
                    You Mean lt
                </h2>
                <h2 class="italic">Martin Garrix</h2>

            </div>
            <div class="col-7 px-5">
                <p class="small">As a coach and mentor, my ultimate goal is to motivate visual artists
                    toward inspired action. I help you get you back on track to being the
                    productive, creative, meaningful and authentic artist you truly want
                    to be.l support artists in crafting and living a creative life as well as
                    feeling good about themselves and their art.</p>
                <p class="small">As an artist and an educator for nearly 30 years, I understand what it
                    takes to create.</p>
                <button class="btn feat-btn">Get started today</button>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.bold {
    font-weight: 800;
    font-size: 2.5rem;
}

.background-1 {
    position: absolute;
    top: 10%;
    left: -10%;
    width: 119%;
    opacity: 0.3;
}

.background-2 {
    position: absolute;
    top: 36%;
    left: 71%;
    width: 10%;

}

.background-3 {
    position: absolute;
    top: -11%;
    left: -30%;
    width: 40%;
    transform: rotate(179deg);
}

.background-4 {
    position: absolute;
    top: 41%;
    left: 97%;
    width: 11%;

}

.container {
    position: relative;
    margin-top: 8rem;
}

.title-wrapper {
    width: 47%;
}

.italic {
    font-family: 'Rossela-demo';
    font-size: 3rem;
    color: $hoveredMainBtn;
}

.card-wrapper {
    display: flex;
    margin-top: 3rem;
    height: 250px;
    justify-content: space-evenly;
}

.card {
    width: 200px;
    height: 230px;
    border: none;
    background: transparent;

    p {
        font-size: .8rem;
    }

    img {
        width: 50%;
    }
}

h5 {
    font-weight: 800;
}

.feat-btn {
    background: #ef70313b;
    color: #EF6F31;
    font-weight: 900;
    margin-top: 1rem;

    &:hover {
        background-color: $mainBtn;
        color: white;
    }
}
</style>