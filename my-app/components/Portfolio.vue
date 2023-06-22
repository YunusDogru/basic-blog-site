<template>
  <div class="portfolio-carousel">
    <div class="portfolio-header">
        <span>Our Team</span>
        <h2>People Behind Success</h2>
    </div>
    <div class="carousel-boxes"  ref="carousel"
    @mousedown="dragStart"
    @touchstart="dragStart" 
    @mousemove="dragging"
    @touchmove="dragging"
    @mouseup="dragStop"
    @touchend="dragStop"
    @mouseleave="dragStop"
    >
        <div class="carousel-box" ref="firstBox">
            <div class="carousel-image"><img src="https://webangon.com/html/bisness/img/portfolio/1.jpg" draggable="false"/></div>
            <div class="carousel-content">
                <h4>Beff Baffer Bussines</h4>
                <span>Financial Construction</span>
            </div>
        </div>
        <div class="carousel-box">
            <div class="carousel-image"><img src="https://webangon.com/html/bisness/img/portfolio/2.jpg" draggable="false"/></div>
            <div class="carousel-content">
                <h4>Beff Baffer Bussines</h4>
                <span>Financial Construction</span>
            </div>
        </div>
        <div class="carousel-box">
            <div class="carousel-image"><img src="https://webangon.com/html/bisness/img/portfolio/3.jpg" draggable="false"/></div>
            <div class="carousel-content">
                <h4>Beff Baffer Bussines</h4>
                <span>Financial Construction</span>
            </div>
        </div>
        <div class="carousel-box">
            <div class="carousel-image"><img src="https://webangon.com/html/bisness/img/portfolio/4.jpg" draggable="false"/></div>
            <div class="carousel-content">
                <h4>Beff Baffer Bussines</h4>
                <span>Financial Construction</span>
            </div>
        </div>
        <div class="carousel-box">
            <div class="carousel-image"><img src="https://webangon.com/html/bisness/img/portfolio/5.jpg" draggable="false"/></div>
            <div class="carousel-content">
                <h4>Beff Baffer Bussines</h4>
                <span>Financial Construction</span>
            </div>
        </div>
        <div class="carousel-box">
            <div class="carousel-image"><img src="https://webangon.com/html/bisness/img/portfolio/6.jpg" draggable="false"/></div>
            <div class="carousel-content">
                <h4>Beff Baffer Bussines</h4>
                <span>Financial Construction</span>
            </div>
        </div>
    </div>
  </div>
</template>

<script setup>
const carousel = ref();
const firstBox = ref();
const data = reactive({
    isDragStart: false,
    isDragging: false,
    prevPageX: 0,
    prevScrollLeft: 0,
    diff: 0
})
const autoSlide = () => {
    if(carousel.value.scrollLeft == (carousel.value.scrollWidth - carousel.value.clientWidth)) {
        carousel.value.scrollLeft = 0;
    }
    data.diff = Math.abs(data.diff);
    let firstImgWidth = firstBox.value.clientWidth + 30;
    let valDifference = firstImgWidth - data.diff;
    console.log(valDifference);
    if(carousel.value.scrollLeft > data.prevScrollLeft) {
        return carousel.value.scrollLeft += data.diff > firstImgWidth / 3 ? valDifference : -data.diff;
    } else {
        return carousel.value.scrollLeft -= data.diff > firstImgWidth / 3 ? valDifference : -data.diff;
    }
}
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
    carousel.value.classList.add('smooth');

    if(!data.isDragging) return;
    data.isDragging = false;
    autoSlide();
    carousel.value.classList.remove('smooth');
}
</script>

<style scoped>
.smooth {
    scroll-behavior: smooth;
}
.portfolio-carousel {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    padding: 40px 0;
}
.portfolio-header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.portfolio-header span {
    color: rgb(102, 102, 102);
    position: absolute;
    transform: translateY(-50px);
    font-size: 15px;
}
.portfolio-header h2 {
    font-size: 32px;
    font-weight: bold;
}
.carousel-boxes {
    cursor: pointer;
    white-space: nowrap;
    width: 80%;
    padding: 0 auto;
    overflow: hidden;
}
.carousel-box {
    display: inline-block;
    height: fit-content;
    width: calc((100% / 3) - 30px );
    margin-left: 30px;
    border-radius: 5px;
    border: 1px solid rgba(122, 133, 149, 0.3);
}
.carousel-box:first-child {
    margin-left: 0;
}
@media (max-width: 1200px) {
    .carousel-box {
        width: calc(50% - 30px);
    }
}
@media (max-width: 800px) {
    .carousel-box {
        width: calc(100%);
    }
}
.carousel-image {
    width: 100%;
    display: flex;
    height: fit-content;
    position: relative;
}
.carousel-image img {
    width: 100%;
}
.carousel-box:hover .carousel-image:before {
    content: '';
    width: 100%;
    height: 100%;
    position: absolute;
    background-repeat: no-repeat;
    background-image: url("http://webangon.com/html/bisness/img/ro.png");
    animation: carouselBoxAnim 0.3s;
    animation-fill-mode: both;
    background-position-x: 50%;
    background-position-y: 50%;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 10;
}
.carousel-box:hover .carousel-content h4 {
    color: rgb(0, 96, 255);
}

@keyframes carouselBoxAnim {
    to {
        background-color: rgba(34, 35, 40, 0.4);
    }
}

.carousel-content {
    padding: 25px;
}
.carousel-content h4 {
    font-size: 22px;
    margin-bottom: 10px;
    transition: color 0.3s;
}
.carousel-content span {
    font-size: 15px;
    color: rgb(122, 133, 149);
    transition: color 0.3s;
}
</style>