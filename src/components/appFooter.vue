<script>
import { store } from "../store.js" //state management
import register from "../debug" //per debuggare il componente da console

export default {
    name: "appFooter",
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
    <div class="wrapper">
        <div class="me-5">
            <h6 class="fw-bold">Address</h6>
            <ul class="list-unstyled">
                <li>382 NE 191st St # 87394 Miami, FL 33179-3899</li>
                <li>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</li>
                <li>support@maxcoach.com</li>
            </ul>
        </div>

        <div class="me-5">
            <h6 class="fw-bold">Explore</h6>
            <ul class="list-unstyled">
                <li>Start here</li>
                <li>Success story</li>
                <li>Blog</li>
                <li>Courses</li>
                <li>Contact us</li>
            </ul>
        </div>
        <div class="me-5">
            <h6 class="fw-bold">Information</h6>
            <ul class="list-unstyled">
                <li>Membership</li>
                <li>Purchase guide</li>
                <li>Privacy policy</li>
                <li>Terms of services</li>

            </ul>
        </div>
        <div>
            <h6 class="fw-bold">Instagram <span>@maxcoach</span></h6>

        </div>
    </div>
    <div class="text-center mb-3 text-secondary">© 2020 Maxcoach. All Rights Reserved</div>
</template>
<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.wrapper {
    display: flex;
    align-items: flex-start;
    padding: 5rem;
}

li {
    margin: 1rem 0;
    color: gray;
    cursor: pointer;

    &:hover {
        color: $mainBtn;
    }
}

span {
    color: $mainBtn;
}
</style>