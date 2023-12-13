<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "events",
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
    <div class="container">
        <div class="title-wrapper text-center">
            <h2 class="italic">Upcoming Events</h2>
            <h2 class="fw-bold mb-5">Let's work together</h2>
        </div>
        <div class="row">
            <div class="col-12 d-flex justify-content-around">
                <div class="d-flex">
                    <figure class="overflow-hidden">
                        <img src="../assets/images/artist-event-04-250x300.jpg" alt="">
                    </figure>
                    <div class="align-self-center p-5">
                        <p class="text-secondary my-1">APR 22, 2021 </p>
                        <h4 class="fw-bold"> Storytelling Workshop</h4>
                        <p calss="text-secondary">Texas, US</p>
                    </div>
                </div>
                <div class="d-flex">
                    <figure class="overflow-hidden">
                        <img src="../assets/images/artist-event-03-250x300.jpg" alt="">
                    </figure>
                    <div class="align-self-center p-5">
                        <p class="text-secondary my-1">OCT 10, 2020</p>
                        <h4 class="fw-bold">Painting Art Contest 2020</h4>
                        <p calss="text-secondary">New York, US</p>
                    </div>
                </div>
            </div>
            <div class="col-12 d-flex justify-content-around mt-5">
                <div class="d-flex">
                    <div class="align-self-center p-5">
                        <p class="text-secondary my-1">NOV 23, 2020</p>
                        <h4 class="fw-bold">International Art Fair 2020</h4>
                        <p calss="text-secondary"> Hamburg, Germany</p>
                    </div>
                    <figure class="overflow-hidden">
                        <img src="../assets/images/artist-event-02-250x300.jpg" alt="">
                    </figure>
                </div>
                <div class="d-flex">
                    <div class="align-self-center p-5">
                        <p class="text-secondary my-1">DEC 15, 2020</p>
                        <h4 class="fw-bold">Street Performance: Call for Artist</h4>
                        <p calss="text-secondary">Illinois, US</p>
                    </div>
                    <figure class="overflow-hidden">
                        <img src="../assets/images/artist-event-01-250x300.jpg" alt="">
                    </figure>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.title-wrapper {
    width: 47%;
    margin: auto;
    padding: 10rem 0 3rem 0;
}

.italic {
    font-family: 'Rossela-demo';
    font-size: 3rem;
    color: $hoveredMainBtn;
}

img {
    transition: 1s;

    &:hover {
        transform: scale(1.2);
    }
}
</style>