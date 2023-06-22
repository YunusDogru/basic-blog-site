<template>
  <section class="video-wrapper">
    <div class="video-text">
        <h2>Quality makes the<br>belief for customers</h2>
        <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. </p>
        <div class="video-holder">
            <a @click="openPopup">
              <span class="video-btn"><Icon name="material-symbols:play-arrow-rounded"/></span>
            </a>
        </div>
    </div>
  </section>
  <div v-if="showPopup" class="popup" @click="showPopup = false">
    <iframe class="videoPopup" :src="videoUrl" frameborder="0" allowfullscreen></iframe>
    <Icon @click="showPopup = false" class="closePopup" name="material-symbols:cancel-outline-rounded"/>
  </div>
</template>

<script setup>

const showPopup = ref(false);
const videoUrl = 'https://www.youtube.com/embed/7e90gBu4pas?autoplay=1';

function openPopup() {
  showPopup.value = !showPopup.value;
}

</script>

<style scoped>
.popup {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.5);
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 999999;
  width: 100vw;
  height: 100vh;
  outline: 10px solid #fff;
}
.videoPopup {
  width: 80%;
  height: 80%;
  position: relative;
}
.closePopup {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #000;
  color: #fff;
  border-radius: 50%;
  font-size: 25px;
  padding: 0;
  top: 10%;
  right: 10%;
  transform: translate(50%, -50%);
}
.video-wrapper {
    background-image: url("http://webangon.com/html/bisness/img/slider/red.jpg");
    background-color: #000000;
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;
    min-height: 550px;
    padding: 110px 0 80px 0;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}
.video-wrapper::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
}
.video-text {
  width: 80%;
  height: 100%;
  margin-bottom: 30px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: space-between;
}
.video-text * {
  width: 50%;
  color: #fff;
  z-index: 2;
}
@media (max-width: 1000px) {
  .video-text * {
    width: 100%;
  }
}
.video-text h2 {
  font-size: 45px;
  margin-bottom: 25px;
  line-height: 50px;
  font-weight: 700;

}
.video-text p {
  font-size: 16px;
  line-height: 30px;
}
.video-holder {
  height: 125px;
  margin-top: 30px !important;
}
.video-btn {
  background-color: rgb(0, 96, 255);
  height: 65px;
  width: 65px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  font-size: 25px;
  animation: shadowAnim 1.5s ease-out;
  animation-iteration-count: infinite;
}
@keyframes shadowAnim {
  from {
    box-shadow: 0 0 0 0 rgba(0, 0, 0, 0.2);
  }
  to {
    box-shadow: 0 0 0 15px rgba(0, 0, 0, 0);
  }
}

</style>