<template>
    <div class="carousel-text" v-if="visibleSlide === 0">
        <h1 class="carousel-text-header">Global Bussiness Solution</h1>
        <p class="carousel-text-content">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.At vero eos et accusam et justo </p>
        <a class="carousel-text-button" href="#">Contact now</a>
    </div>
    <div class="carousel-text" v-else-if="visibleSlide === 1">
        <h1 class="carousel-text-header">We Build Your Best Buisness</h1>
        <p class="carousel-text-content">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.At vero eos et accusam et justo</p>
        <a class="carousel-text-button" href="#">Contact now</a>
    </div>
</template>

<script setup>
const props = defineProps({
    visibleSlide: {
    type: Number,
    required: true
    }
});
</script>

<style scoped>
.carousel-text {
    z-index: 1;
    color: #fff;
    width: 80%;
    min-height: 40%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    position: absolute;
}
.carousel-text-header {
    position: relative;
    font-size: 60px;
    font-style: normal;
    font-weight: bold;
    line-height: 70px;
    text-align: center;
    animation: textFadeIn 0.6s ease-out;
    animation-delay: 1.1s;
    animation-fill-mode: both;
}
@media (max-width: 800px) {
    .carousel-text-header {
        font-size: 30px;
    }
}
.carousel-text-content {
    margin: 20px 0;
    font-size: 15px;
    font-weight: 500;
    line-height: 30px;
    width: 70%;
    text-align: center;
    animation: textFadeIn 0.6s ease-out;
    animation-delay: 1.3s;
    animation-fill-mode: both;
}
.carousel-text-button {
    height: 60px;
    width: 180px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: none;
    border-radius: 5px;
    background-color: rgb(0, 96, 255);  
    text-decoration: none;
    color: white;  
    animation: textFadeIn 0.6s ease-out;
    animation-delay: 1.5s;
    animation-fill-mode: both;
}
@keyframes textFadeIn {
    from {
        opacity: 0;
        transform: translateY(80px);
    }
    to {
        opacity: 1;
        transform: translateY(0px);
    }

}
</style>