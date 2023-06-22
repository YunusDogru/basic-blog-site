<template>
  <div class="partners-carousel">
    <div class="carousel-boxes"  ref="carousel"
    @mousedown="dragStart" 
    @mousemove="dragging"
    @mouseup="dragStop"
    @mouseleave="dragStop"
    >
        <div class="image-wrapper" ref="firstBox">
            <img src="http://webangon.com/html/bisness/img/brand/1.png">
        </div>
        <div class="image-wrapper">
            <img src="http://webangon.com/html/bisness/img/brand/2.png">
        </div>
        <div class="image-wrapper">
            <img src="http://webangon.com/html/bisness/img/brand/3.png">
        </div>
        <div class="image-wrapper">
            <img src="http://webangon.com/html/bisness/img/brand/4.png">
        </div>
        <div class="image-wrapper">
            <img src="http://webangon.com/html/bisness/img/brand/5.png">
        </div>
        <div class="image-wrapper" v-for="i in numberList" :key="i + 5">
            <img :src="`http://webangon.com/html/bisness/img/brand/${i}.png`">
        </div>
    </div>
  </div>
</template>

<script setup>
const carousel = ref();
const firstBox = ref();


const data = reactive({
    isDragStart: false,
    prevPageX: 0,
    prevScrollLeft: 0,
    diff: 0
})
const numberList = ref(Array.from({ length: 30 }, (_, index) => (index % 5) + 1));

const dragStart = (e) => {
        e.preventDefault();
        data.isDragStart = true;
        data.prevPageX = e.pageX || e.touches[0].pageX;
        data.prevScrollLeft = carousel.value.scrollLeft;
}
const dragging = (e) => {
    if(data.isDragStart) {
        e.preventDefault();
        data.isDragging = true;
        data.diff = (e.pageX || e.touches[0].pageXd)- data.prevPageX;
        carousel.value.scrollLeft = data.prevScrollLeft - data.diff;
    }
}
const dragStop = () => {
    data.isDragStart = false;
}
</script>

<style scoped>
.smooth {
    scroll-behavior: smooth;
}
.partners-carousel {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    padding: 80px 0;
}
.carousel-boxes {
    cursor: pointer;
    white-space: nowrap;
    width: 80%;
    padding: 0 auto;
    overflow: hidden;
}
.image-wrapper {
    display: inline-block;
    width: 20%;
    text-align: center;
}

@media (max-width: 1200px) {
    .image-wrapper {
        width: 25%;
    }
}

@media (max-width: 1000px) {
    .image-wrapper {
        width: calc(100% / 3);
    }
}
@media (max-width: 750px) {
    .image-wrapper {
        width: 50%;
    }
}

</style>