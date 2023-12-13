<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "newsletterForm",
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
    <section>
        <img class="background-1" src="../assets/images/artist-shape-color-paint-bottom-right.png" alt="">
        <img class="background-2" src="../assets/images/artist-shape-color-paint-top-left.png" alt="">
        <div class="wrapper">
            <div class="d-flex">
                <h2>Newsletter to get in touch</h2>
                <div class="input-group mb-3">
                    <input type="email" class="my-form" placeholder="Your e-mail" aria-label="Your e-mail"
                        aria-describedby="button-addon2">
                    <button class="arrow" type="button" id="button-addon2"><i class="fa fa-arrow-right"
                            aria-hidden="true"></i></button>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

section {
    background-color: #244186;
    overflow: hidden;
    margin: 10rem 0;
    position: relative;
}

.background-1 {
    position: absolute;
    bottom: 0%;
    right: 0%;
}

.background-2 {
    position: absolute;
    top: 0%;
    left: 0%;
}

.wrapper {
    width: 75%;
    margin: auto;
    padding: 3rem;
}

h2 {
    font-family: 'Times New Roman', Times, serif;
    color: white;
    margin-right: 5rem;
}

.my-form {
    background-color: transparent;
    color: white;
    border: none;
    border-bottom: 2px solid white;
    width: 600px;


}

.arrow {
    border: none;
    border-bottom: 2px solid white;
    color: white;
    background: transparent;
}

::placeholder {
    color: white;
}
</style>