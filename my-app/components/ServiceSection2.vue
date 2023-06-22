<template>
  <section class="section-wrapper">
    <div class="section-text">
        <h2>Quality makes the<br>belief for customers</h2>
        <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. </p>
        <a href="#" class="section-btn">Get A Free Quote</a>
    </div>
  </section>
</template>

<style scoped>
.section-wrapper {
    background-image: url("http://webangon.com/html/bisness/img/slider/bg9.jpg");
    background-color: #000000;
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;
    min-height: 550px;
    padding: 110px 0 80px 0;
    position: relative;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
}
.section-wrapper::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
}
.section-text {
  width: 40%;
  height: 100%;
  margin-bottom: 30px;
  margin-right: 10%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  justify-content: space-between;
}
.section-text * {
  color: #fff;
  z-index: 2;
}
@media (max-width: 1000px) {
  .section-text {
    width: 80%;
    margin: 0 10%;
  }
}
.section-text h2 {
  font-size: 2.5rem;
  margin-bottom: 25px;
  line-height: 50px;
  font-weight: 700;

}
.section-text p {
  font-size: 16px;
  line-height: 30px;
}

.section-btn {
  background-color: rgb(0, 96, 255);
  text-decoration: none;
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: flex-start;
  border-radius: 5px;
  font-size: 15px;
  padding: 0 2rem;
  margin-top: 20px;
  height: 3rem;
}

</style>