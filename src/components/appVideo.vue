<template>
    <div class="container d-flex justify-content-center ">
        <button @click="showVideo" id="btn">
            <img id="poster" src="../assets/images/artist-video-poster.jpg" alt="">
            <img id="youtube" src="../assets/images/icon-youtube-play.png" alt="">

        </button>
        <div v-if="videoVisible">
            <div id="video"></div>
            <div id="overlay">
                <div id="video-container">
                    <iframe width="560" height="315" src="https://www.youtube.com/embed/OMOga8x6aLk" frameborder="0"
                        allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    name: "appVideo",
    data() {
        return {
            videoVisible: false,
        };
    },
    methods: {
        showVideo() {
            this.videoVisible = true;
        },
        closeVideo(e) {
            const video = this.$el.querySelector('#video');
            const overlay = this.$el.querySelector('#overlay');
            const videoContainer = this.$el.querySelector('#video-container');


            if (!video.contains(e.target)) {
                this.videoVisible = false;

                videoContainer.innerHTML = '';
            }
        },

    },
    mounted() {
        document.addEventListener('touchend', this.closeVideo);
        document.addEventListener('mouseup', this.closeVideo);
    },
    beforeDestroy() {
        document.removeEventListener('touchend', this.closeVideo);
        document.removeEventListener('mouseup', this.closeVideo);
    },
};
</script>
  
<style scoped lang="scss">
.container {
    margin-top: 10rem;
    margin-bottom: 10rem;
}

#overlay {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    top: 0;
    left: 0;
    z-index: 3;
    height: 100vh;
    width: 100%;
    background: black;
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
  