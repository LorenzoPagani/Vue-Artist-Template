<template>
    <p>{{ countdown }}</p>
</template>
  
<script>
export default {
    data() {
        return {
            countdown: '',
            countDownDate: new Date("dec 15, 2023 15:37:25").getTime(),
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
  
<style scoped>
p {
    font-size: 1.5rem;
    margin-bottom: 0;
    margin-left: 1rem;
    color: #3F3A64;
    font-weight: 800;
}
</style>
  