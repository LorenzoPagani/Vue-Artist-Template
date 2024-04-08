<template>
    <p>{{ countdown }}</p>
</template>

<script>
export default {
    data() {
        return {
            countdown: '',
            countDownDate: new Date(new Date().getTime() + 24 * 60 * 60 * 1000),
        };
    },
    mounted() {
        this.updateCountdown();
        this.timerInterval = setInterval(this.updateCountdown, 1000);
    },
    beforeDestroy() {
        clearInterval(this.timerInterval);
    },
    methods: {
        updateCountdown() {
            const now = new Date().getTime();
            const distance = this.countDownDate - now;

            if (distance >= 0) {
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);

                this.countdown = `${days}d ${hours}h ${minutes}m ${seconds}s`;
            } else {
                clearInterval(this.timerInterval);
                this.countdown = "EXPIRED";
            }
        },
    },
};
</script>

<style scoped lang="scss">
@use '../styles/partials/variables' as *;

p {
    font-size: 1.5rem;
    margin-bottom: 0;
    margin-left: 1rem;
    color: $secondColor;
    font-weight: 800;
}
</style>