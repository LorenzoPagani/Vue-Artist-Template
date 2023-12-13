<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console
import jumbo from "../components/jumbo.vue"
import countdown from "../components/countdown.vue"

export default {
    name: "appHeader",
    components: {
        jumbo,
        countdown
    },
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
    <header>
        <div id="event-banner">
            <!-- toDo: add countdown -->
            Our biggest event starts tomorrow
            <countdown /> <button class="btn main-btn"> get ticket</button>
        </div>
        <div class="container">
            <div class="row nav-bar p-3">
                <a href="#" class="header-logo col-4">
                    <img src="../assets/images/dark-logo.png" alt="">
                </a>
                <div class="col-4">
                    <nav class="d-flex">
                        <!-- toDo: add dropdown -->
                        <a href="#">features </a>
                        <a href="#">testimonials </a>
                        <a href="#">catalogue </a>
                        <a href="#">blog </a>
                        <a href="#">events </a>
                    </nav>
                </div>
                <div class="col-4 socials">
                    <a href="#"><i class="fa-brands fa-twitter text-dark mx-2" aria-hidden="true"></i></a>
                    <a href="#"><i class="fa-brands fa-facebook-f text-dark mx-2" aria-hidden="true"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram text-dark mx-2" aria-hidden="true"></i></a>
                    <a href="#"><i class="fa-brands fa-linkedin text-dark mx-2" aria-hidden="true"></i></a>
                </div>
            </div>
        </div>
        <jumbo></jumbo>
    </header>
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

a {
    &:hover {
        color: $mainBtn;
    }
}

#event-banner {
    background-color: #F5F5F5;
    padding: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;


}

.main-btn {
    margin-left: 1rem;
    @include main-button()
}

.header-logo {
    img {
        width: 100px;
    }
}

nav {
    justify-content: space-between;

    a {
        text-decoration: none;
        color: black;
    }
}

.socials {
    text-align: end;
}
</style>