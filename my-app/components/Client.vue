<template>
  <section class="client-carousel">
    <div class="client-header">
        <h2>Our Client Review</h2>
        <span>Rearrange the entire color palette, making your site unique and beatiful. Theme useing a wide selection</span>
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
          <div class="wrapper">
              <div class="carousel-header">
                <img src="http://webangon.com/html/bisness/img/all/pro1.jpg" alt="">
                <div class="header-text">
                    <h3>Rose Garle</h3>
                    <span>CEO, Company</span>
                </div>
            </div>
            <p class="carousel-content">
                Exercitation ullamco laboris nisi ut alloquip ex ea com <br> modo consequat. Duisaute irure dolor in repre <br> hender itin.
            </p>
          </div>
        </div>
       <div class="carousel-box">
          <div class="wrapper">
              <div class="carousel-header">
                <img src="http://webangon.com/html/bisness/img/all/pro1.jpg" alt="">
                <div class="header-text">
                    <h3>Rose Garle</h3>
                    <span>CEO, Company</span>
                </div>
            </div>
            <p class="carousel-content">
                Exercitation ullamco laboris nisi ut alloquip ex ea com <br> modo consequat. Duisaute irure dolor in repre <br> hender itin.
            </p>
          </div>
        </div>
        <div class="carousel-box">
          <div class="wrapper">
              <div class="carousel-header">
                <img src="http://webangon.com/html/bisness/img/all/pro1.jpg" alt="">
                <div class="header-text">
                    <h3>Rose Garle</h3>
                    <span>CEO, Company</span>
                </div>
            </div>
            <p class="carousel-content">
                Exercitation ullamco laboris nisi ut alloquip ex ea com <br> modo consequat. Duisaute irure dolor in repre <br> hender itin.
            </p>
          </div>
        </div>
        <div class="carousel-box">
          <div class="wrapper">
              <div class="carousel-header">
                <img src="http://webangon.com/html/bisness/img/all/pro1.jpg" alt="">
                <div class="header-text">
                    <h3>Rose Garle</h3>
                    <span>CEO, Company</span>
                </div>
            </div>
            <p class="carousel-content">
                Exercitation ullamco laboris nisi ut alloquip ex ea com <br> modo consequat. Duisaute irure dolor in repre <br> hender itin.
            </p>
          </div>
        </div>
        <div class="carousel-box">
          <div class="wrapper">
              <div class="carousel-header">
                <img src="http://webangon.com/html/bisness/img/all/pro1.jpg" alt="">
                <div class="header-text">
                    <h3>Rose Garle</h3>
                    <span>CEO, Company</span>
                </div>
            </div>
            <p class="carousel-content">
                Exercitation ullamco laboris nisi ut alloquip ex ea com <br> modo consequat. Duisaute irure dolor in repre <br> hender itin.
            </p>
          </div>
        </div>
        <div class="carousel-box">
          <div class="wrapper">
              <div class="carousel-header">
                <img src="http://webangon.com/html/bisness/img/all/pro1.jpg" alt="">
                <div class="header-text">
                    <h3>Rose Garle</h3>
                    <span>CEO, Company</span>
                </div>
            </div>
            <p class="carousel-content">
                Exercitation ullamco laboris nisi ut alloquip ex ea com <br> modo consequat. Duisaute irure dolor in repre <br> hender itin.
            </p>
          </div>
        </div>
    </div>
  </section>
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
.client-carousel {
    position: relative;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    padding: 40px 0 100px 0;
    background-image: url("http://webangon.com/html/bisness/img/all/testibg.jpg");
    background-size: cover;
    background-repeat: no-repeat;
}
.client-carousel::after {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(255, 255, 255, 0.9);
    z-index: 2;
}
.client-header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    z-index: 3;
}
.client-header span {
    color: rgb(102, 102, 102);
    font-size: 15px;
    max-width: 500px;
    line-height: 30px;
}
.client-header h2 {
    font-size: 32px;
    font-weight: bold;
}
.carousel-boxes {
    cursor: pointer;
    white-space: nowrap;
    width: 80%;
    padding: 0 auto;
    overflow: hidden;
    background-color: transparent;
    z-index: 3;

}
.carousel-box {
    display: inline-block;
    height: fit-content;
    width: calc(50% - 30px);
    margin-left: 30px;
    padding: 30px 30px 30px 60px;
    border-radius: 5px;
    border: 1px solid rgba(122, 133, 149, 0.3);
    z-index: 3;
    background-color: #fff;
}
@media (max-width: 1200px) {
    .carousel-boxes {
        width: 60% !important;
    }
    .carousel-box {
        width: 100% !important;
    }
}
@media (max-width: 800px) {
    .carousel-boxes {
        width: 80% !important;
    }
    .carousel-box {
        width: 100% !important;
    }
}
.wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: flex-start;
}
.wrapper .carousel-header {
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
}
.carousel-header img {
    width: 95px;
    border-radius: 50%;
}
.header-text {
    padding: 25px 0 0 45px;
}
.header-text h3 {
    color: #000;
    font-size: 20px;
    font-weight: bold;
    line-height: 24px;
    margin-bottom: 8px;
    text-align: left;
}
.header-text span {
    color: rgb(102, 102, 102);
    font-size: 15px;
    font-weight: 600;
    line-height: 22.5px;
    text-align: left;
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
.carousel-content {
    line-height: 30px;
    color: rgba(122, 133, 149);
    font-size: 13px;
    font-weight: 500;
    padding-top: 25px;
}
</style>
