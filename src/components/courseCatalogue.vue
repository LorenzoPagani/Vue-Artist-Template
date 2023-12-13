<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "courseCatalogue",
    data() {
        return {
            store,
            courseCards: [
                {
                    img: this.getImagePath("../assets/images/artist-course-01-480x480.jpg"),
                    price: "$18.00",
                    text: "The Acrylic Painting Academy"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-02-480x480.jpg"),
                    price: "$18.00",
                    text: "Drawing and Shading: Complete Course"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-03-480x480.jpg"),
                    price: "$18.00",
                    text: "The Color Theory for Digital Artist"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-04-480x480.jpg"),
                    price: "$18.00",
                    text: "Ultimate Guide to Digital Sketching for Beginner"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-05-480x480.jpg"),
                    price: "$18.00",
                    text: "Portrait Drawing The Smart Way"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-06-480x480.jpg"),
                    price: "$18.00",
                    text: "Mastering Watercolor Painting from Beginner"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-07-480x480.jpg"),
                    price: "$18.00",
                    text: "The Art & Science of Drawing"
                },
                {
                    img: this.getImagePath("../assets/images/artist-course-08-480x480.jpg"),
                    price: "$18.00",
                    text: "The Colored Pencil Drawing Course"
                },
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`${img}`, import.meta.url).href
        }
    },
    mounted() {
        register(this); //per debuggare il componente da console

    }
}
</script>
<template>
    <div id="catalogue" class="wrapper text-center ">
        <img :style="{ left: 25.37 + store.mouseX + '%', top: 50.47 + store.mouseY + '%' }"
            class="position-absolute shape-1 " src="../assets/images/artist-shape-01.png" alt="">
        <h2 class="italic ">Artist coaching</h2>
        <h2 class="fw-bold">Latest Online Courses</h2>
    </div>
    <div class="card-wrapper d-flex flex-wrap">
        <div v-for="card in courseCards" class="my-card">
            <figure class="overflow-hidden">
                <img class="w-100" :src="card.img" alt="">
            </figure>
            <div class="p-3 textbox">
                <p class="price">{{ card.price }}</p>
                <p>{{ card.text }}</p>
            </div>
        </div>
    </div>
    <div class="text-center">
        <button class="btn">Get started today</button>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.wrapper {
    margin-top: 5rem;
    position: relative;
}

.shape-1 {
    width: 30%;
    color: #EF6F31;
    z-index: -1
}

.italic {
    font-family: 'Rossela-demo';
    font-size: 3rem;
    color: $hoveredMainBtn;
}

.my-card {
    width: calc(100% / 4 - 4rem);
    margin: 1rem 2rem 0 2rem;
    overflow: hidden;
    transition: 1s;

    .textbox {
        background: white;
    }

    &:hover {

        img {
            transition: 1s;
            transform: scale(1.2);
        }

        .textbox {
            border: 1px solid $mainBtn;
            position: relative;
            bottom: 15%;
        }
    }
}

.btn {
    background: #ef70313b;
    color: #EF6F31;
    font-weight: 900;
    margin-top: 1rem;

    &:hover {
        background-color: $mainBtn;
        color: white;
    }
}

.price {
    color: $mainBtn;
    font-weight: bold;
}
</style>