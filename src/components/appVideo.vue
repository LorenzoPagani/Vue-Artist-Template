<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "appVideo",
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
    <div class="wrapper position-relative">
        <img class="wave" src="../assets/images/wave.svg" alt="">
        <div class="container text-center mt-5">
            <iframe width="970" height="570" src="https://www.youtube.com/embed/ROa9p2f2jjE?si=WrWA3GRZ0zDwfdjc"
                title="YouTube video player" poster="" allowfullscreen>
            </iframe>
        </div>
    </div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

iframe {
    margin-top: 5rem;
    border-radius: 5px;
}

.wave {
    height: 300px;
    width: 100%;
    background: #FAF8F6;
    position: absolute;
    top: 58%;
    z-index: -1;
}
</style>