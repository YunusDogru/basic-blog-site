<template>
  <section class="service-section">
    <h3>
        Do You Have A Project We Can Help With?we provide our best Privacy & Policy best idea!.
    </h3>
    <a href="#"># Get a free quote</a>
  </section>
</template>>

<style scoped>

.service-section {
    height: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-image: url("http://webangon.com/html/bisness/img/slider/slide1.jpg");
    position: relative;
}
.service-section::before {
    content: "";
    background-color: rgba(22, 24, 25, 0.5);
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
}

.service-section h3 {
    color: #fff;
    font-size: 2.5rem;
    font-weight: bold;
    line-height: 4rem;
    margin-bottom: 8px;
    text-align: center;
    max-width: 70%;
    z-index: 3;
}
.service-section a {
    text-decoration: none;
    color: #fff;
    height: 55px;
    padding: 0 2rem;
    margin-top: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgb(0, 96, 255);
    border-radius: 5px;
    font-size: 15px;
    font-weight: 500;
    z-index: 3;
}
</style>