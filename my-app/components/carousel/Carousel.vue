<template>
    <section class="carousel"
        ref="carousel"
        @mousedown="dragStart"
        @touchstart="dragStart" 
        @mousemove="dragging"
        @touchmove="dragging"
        @mouseup="dragStop"
        @touchend="dragStop"
        @mouseleave="dragStop">
        <carousel-slide 
            v-for="(slide, index) in slides" 
            :key="slide" 
            :index="index"
            :visibleSlide="visibleSlide"
            :direction="direction"
            >
            <img class="carousel-image" 
                :src="slide" 
                draggable="false" 
                @mousedown="dragStart"
                @touchstart="dragStart" 
                @mousemove="dragging"
                @touchmove="dragging"
                @mouseup="dragStop"
                @touchend="dragStop"
                @mouseleave="dragStop"
                >
        </carousel-slide>
        <div @click="next" class="next"><Icon name="ic:outline-keyboard-arrow-right"/></div>
        <div @click="prev" class="prev"><Icon name="ic:outline-keyboard-arrow-left"/></div>
        <carousel-text :visibleSlide="visibleSlide"/>
    </section>
</template>

<script setup>
const carousel = ref();


const slides = [
  'http://webangon.com/html/bisness/img/slider/bg4.jpg',
  'http://webangon.com/html/bisness/img/slider/bg5.jpg',
];
const visibleSlide = ref(0);
const direction = ref('left');
const slidesLen = computed(() => slides.length);

const next = () => {
  if (visibleSlide.value >= slidesLen.value - 1) {
    visibleSlide.value = 0;
  } else {
    visibleSlide.value++;
  }
  direction.value = 'left';
};

const prev = () => {
  if (visibleSlide.value <= 0) {
    visibleSlide.value = slidesLen.value - 1;
  } else {
    visibleSlide.value--;
  }
  direction.value = 'right';

};
const data = reactive({
    isDragStart: false,
    isDragging: false,
    prevPageX: 0,
    prevScrollLeft: 0,
    diff: 0
})

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
    if(data.diff < 0) {
        next();
    } else if (data.diff > 0) {
        prev();
    }
    data.diff = 0;
}

</script>

<style scoped>
    .carousel {
        position: relative;
        width: 100vw;
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .carousel .next, .carousel .prev {
        width: 60px;
        height: 60px;
        position: absolute;
        top: calc(50% - 30px);
        background-color: rgb(0, 96, 255);
        font-size: 25px;
        display: none;
        color: #fff;
        border-radius: 5px;
    }
    .carousel:not(:hover) .left,
    .carousel:not(:hover) .right {
        display: none;
    }
    .carousel:hover .prev {
        animation: fadeInRight 0.3s ease-in-out;
        animation-fill-mode: forwards;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    @keyframes fadeInRight {
        from {
            opacity: 0;
            left: -100px;
        }
        to {
            opacity: 1;
            left: 40px;
        }
    }
    .carousel:hover .next {
        animation: fadeInLeft 0.3s ease-in-out;
        animation-fill-mode: forwards;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    @keyframes fadeInLeft {
        from {
            opacity: 0;
            right: -100px;
        }
        to {
            opacity: 1;
            right: 40px;
        }
    }
    
    .carousel-image {
        height: 100%;
        width: 100%;
        overflow: hidden;
        object-fit: cover;
        position: relative;
    }
</style>