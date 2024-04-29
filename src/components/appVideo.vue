<template>
    <div class="container d-flex justify-content-center ">
        <img :style="{ left: 0.5 + store.mouseX + '%', top: -14.47 + store.mouseY + '%' }"
            class="position-absolute z-0 shape-1" src="../assets/images/stain.svg" alt="">
        <img :style="{ left: 0.5 - store.mouseX + '%', top: -14.47 - store.mouseY + '%' }"
            class="position-absolute  shape-1" src="../assets/images/maxcoach-shape-05-150x150.png" alt="">
        <div class="circle position-absolute"
            :style="{ right: -2.5 + store.mouseX + '%', top: + 14.47 - store.mouseY + '%' }"></div>
        <img :style="{ right: 2.5 - store.mouseX + '%', top: 65 - store.mouseY + '%' }"
            class="position-absolute  shape-1" src="../assets/images/maxcoach-shape-12-150x150.png" alt="">

        <button data-bs-toggle="modal" data-bs-target="#videoModal" id="btn">
            <img id="poster" src="../assets/images/artist-video-poster.jpg" alt="">
            <img id="youtube" src="../assets/images/icon-youtube-play.png" alt="">

        </button>
        <div class="modal fade" id="videoModal">
            <div class="modal-dialog modal-dialog-centered">
                <div class="modal-content bg-transparent border-0">

                    <div id="video-container ">
                        <iframe width="560" height="315" src="https://www.youtube.com/embed/OMOga8x6aLk" frameborder="0"
                            allowfullscreen></iframe>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from "../store.js" //state management

export default {
    name: "appVideo",
    data() {
        return {
            store,
        };
    },
    methods: {

    },
    mounted() {
    },

};
</script>

<style scoped lang="scss">
.container {
    margin-top: 10rem;
    margin-bottom: 10rem;
    position: relative;
}

.shape-1 {
    width: 15%;
}

.circle {
    height: 90px;
    width: 90px;
    border: 12px solid #ECC5AB;
    border-radius: 50%;
}


#btn {
    position: relative;
    border: none;
    display: block;
    width: 970px;
    height: 570px;
    overflow: hidden;
    border-radius: 10px;


    #poster {
        transition: 1.5s;
        object-fit: cover;
        width: 970px;
        height: 570px;

        &:hover {
            transform: scale(1.1);
        }
    }

    #youtube {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, 0%);

    }
}
</style>