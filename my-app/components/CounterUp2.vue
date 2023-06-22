<template>

<section class="counter-up" ref="counterRef">
    <div class="counter-content">
        <div class="row1">
            <Icon class="counter-icon" name="ph:bell-thin"/>
        </div>
        <div class="row2">
            <h2>{{counterValues.value1.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
            <span>HAPPY CLIENTS</span>
        </div>
    </div>
    <div class="counter-content">
        <div class="row1">
            <Icon class="counter-icon" name="clarity:group-line"/>
        </div>
        <div class="row2">
            <h2>{{counterValues.value2.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
            <span>SKILLED TEAM</span>
        </div>
    </div>
    <div class="counter-content">
        <div class="row1">
            <Icon class="counter-icon" name="ph:thumbs-up-light"/>
        </div>
        <div class="row2">
            <h2>{{counterValues.value3.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
            <span>COMPLETE JOB</span>
        </div>
    </div>
    <div class="counter-content">
        <div class="row1">
            <Icon class="counter-icon" name="game-icons:trophy-cup"/>
        </div>
        <div class="row2">
            <h2>{{counterValues.value4.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
            <span>AWARDS WIN</span>
        </div>
    </div>
</section>

</template>

<script setup>

const counterRef = ref(null);
const counterValues = reactive({
    value1: 0,
    value2: 0,
    value3: 0,
    value4: 0
})
const finalValues = [16521, 6420, 13208, 1652];

const startCounter = () => {
  const counterInterval1 = setInterval(() => {
    if (counterValues.value1 < finalValues[0]) {
      counterValues.value1 += Math.floor(finalValues[0] / 30);
      counterValues.value1 = Math.min(counterValues.value1, finalValues[0]);
    } else {
      clearInterval(counterInterval1);
    }
  }, 60);
  const counterInterval2 = setInterval(() => {
    if (counterValues.value2 < finalValues[1]) {
      counterValues.value2 += Math.floor(finalValues[1] / 30);
      counterValues.value2 = Math.min(counterValues.value2, finalValues[1]);
    } else {
      clearInterval(counterInterval2);
    }
  }, 60);
  const counterInterval3 = setInterval(() => {
    if (counterValues.value3 < finalValues[2]) {
      counterValues.value3 += Math.floor(finalValues[2] / 30);
      counterValues.value3 = Math.min(counterValues.value3, finalValues[2]);
    } else {
      clearInterval(counterInterval3);
    }
  }, 60);
  const counterInterval4 = setInterval(() => {
    if (counterValues.value4 < finalValues[3]) {
      counterValues.value4 += Math.floor(finalValues[3] / 30);
      counterValues.value4 = Math.min(counterValues.value4, finalValues[3]);
    } else {
      clearInterval(counterInterval3);
    }
  }, 60);
};

onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        startCounter();
        observer.unobserve(counterRef.value);
      }
    });
  });

  observer.observe(counterRef.value);
});
</script>

<style scoped>
.counter-up {
    background-image: url("http://webangon.com/html/bisness/img/slider_03.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    padding: 110px 0 80px 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
    color: #fff;
    position: relative;
}
.counter-up::after {
    background-color: rgba(0, 123, 255, 0.85);
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
}
.counter-content {
    width: calc(25% - 20px);
    height: fit-content;
    margin: 0 15px 30px 15px;
    display: flex;
    flex-direction: row;
    align-items: center;
    z-index: 3;
    margin: 20px 10px;
}
@media (max-width: 1200px) {
    .counter-up {
        padding: 40px 0;
    }
}
@media (max-width: 1000px) {
    .counter-up {
        padding: 80px 0 50px 0;
    }
    .counter-content {
        width: 45%;
    }
}
.row1 {
    border-right: 2px solid #fff;
}
.counter-icon {
    font-size: 40px;
    margin: 10px 20px;
}
.row2 {
    padding: 20px;
}
.row2 h2{
    font-size: 28px;
    font-weight: 700;
    line-height: 30px;
    margin-bottom: 10px;
    text-align: left;
}
.row2 span {
    font-size: 13px;
    font-weight: 600;
    line-height: 16px;
    text-align: left;
    text-transform: uppercase;
}
</style>