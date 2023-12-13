<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "appBlog",
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
    <div id="blog" class="wrapper">
        <div class="container">
            <div class="title-wrapper text-center">
                <h2 class="italic">Articles and Tips</h2>
                <h2 class="fw-bold mb-5">Latest From The Blog</h2>
            </div>
            <div class="row">
                <div class="card-wrapper col-12">
                    <div class="card">
                        <img src="../assets/images/artist-blog-03-480x356.jpeg" alt="">
                        <div class="p-3">
                            <h4 class="my-3 text-secondary">ARTIST</h4>
                            <h4 class="fw-bold color">Brush Strokes Energize Trees in Paintings</h4>
                            <p class="text-secondary">May 15, 2020</p>
                            <p class="text-secondary">2,004 views</p>
                        </div>
                    </div>
                    <div class="card big offset">
                        <img src="../assets/images/artist-blog-02-500x680.jpg" alt="">
                        <div class="p-3 test">
                            <h4 class="my-3 text-white">ARTIST</h4>
                            <h4 class="fw-bold text-white">Brush Strokes Energize Trees in Paintings</h4>
                            <p class="text-white">May 15, 2020</p>
                            <p class="text-white">2,004 views</p>
                        </div>
                    </div>
                    <div class="card offset">
                        <img src="../assets/images/artist-blog-01-480x356.jpg" alt="">
                        <div class="p-3">
                            <h4 class="my-3 text-secondary">ARTIST</h4>
                            <h4 class="fw-bold color">
                                Pocket-Sized Notebooks
                                Hold Miniature Paintings</h4>
                            <p class="text-secondary">May 15, 2020</p>
                            <p class="text-secondary">3,504 views</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-12 text-center my-5">
                    <p class="text-secondary">Get into details now? <a class="link" href="#">View
                            all
                            posts <i class="fa-solid fa-arrow-right" aria-hidden="true"></i></a></p>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;


.wrapper {
    margin-top: 10rem;
    background-color: #F5F7FA;
    background-image: url(../assets/images/maxcoach-shape-03.png);
    background-repeat: no-repeat;
    background-position: center;
}

.title-wrapper {
    width: 47%;
    margin: auto;
    padding: 5rem 0 3rem 0;
}

.italic {
    font-family: 'Rossela-demo';
    font-size: 3rem;
    color: $hoveredMainBtn;
}

.card-wrapper {
    margin-bottom: 5rem;
    margin-top: 3rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.card {
    width: 250px;
    margin: 0 3rem;
    overflow: hidden;
    transition: 1s;

    &:hover {
        img {
            transform: scale(1.2);
        }
    }

    img {
        width: 100%;
        transition: 1s;
    }

    .color {
        color: $secondColor;
    }
}

.big {
    width: 400px;
    height: 635px;
    background-color: transparent;
    position: relative;
    overflow: hidden;

    img {
        position: static;
        height: 100%;
        object-fit: cover;
        transition: 1s;


        &:hover {
            transform: scale(1.2);
        }
    }

    .test {
        position: absolute;
        top: 60%;
    }
}

.offset {
    position: relative;
    bottom: 10%;
}

.link {
    color: $mainBtn;
    font-weight: bold;
}
</style>