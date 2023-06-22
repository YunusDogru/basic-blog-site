<template>

<section class="counter-up" ref="counterRef">
    <div class="counter-content">
        <img src="http://webangon.com/html/bisness/img/icon/1.png" >
        <h2>{{counterValues.value1.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
        <span>Happy Customers</span>
    </div>
    <div class="counter-content">
        <img src="http://webangon.com/html/bisness/img/icon/2.png" >
        <h2>{{counterValues.value2.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
        <span>Running Design</span>
    </div>
    <div class="counter-content">
        <img src="http://webangon.com/html/bisness/img/icon/3.png" >
        <h2>{{counterValues.value3.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
        <span>Coffee Cups</span>
    </div>
    <div class="counter-content">
        <img src="http://webangon.com/html/bisness/img/icon/4.png" >
        <h2>{{counterValues.value4.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h2>
        <span>Complete Project</span>
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
const finalValues = [35000, 15250, 9270, 52300];

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
    background-color: rgb(0, 96, 255);
    padding: 110px 0 80px 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
    color: #fff;
}
.counter-content {
    width: 22%;
    height: fit-content;
    margin: 0 15px 30px 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.counter-content img {
    height: 30px;
    margin-bottom: 30px;
}
.counter-content h2 {
    font-size: 36px;
    margin-bottom: 5px;
    font-weight: bold;
}
.counter-content span {
    font-size: 16px;
    margin-top: 8px;
    font-weight: 500;
}
@media (max-width: 1200px) {
    .counter-up {
        padding: 40px 0;
    }
}
@media (max-width: 1000px) {
    .counter-up {
        padding: 110px 0 80px 0;
    }
    .counter-content {
        width: 45%;
    }
}
</style>