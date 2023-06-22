<template>
  <section class="subLinks-first">
    <h1>{{header}}</h1>
    <span>
        <a href="#">{{links[0]}}</a>
        /
        <a href="#">{{links[1]}}</a>
    </span>
  </section>

</template>

<script setup>

const props = defineProps({
  header: String,
  links: Array
});

</script>

<style scoped>
.subLinks-first {
    height: 400px;
    width: 100vw;
    display: flex;
    position: relative;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-image: url("http://webangon.com/html/bisness/img/slider/bg-8.jpg");
    background-size: cover;
    background-repeat: repeat;
    background-attachment: fixed;
}
.subLinks-first::after {
    content : "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0,0,0,0.5);
}
.subLinks-first h1 {
    color: #fff;
    font-size: 45px;
    font-weight: 700;
    line-height: 54px;
    margin-bottom: 10px;
    z-index: 2;
}
.subLinks-first span {
    color: #fff;
    z-index: 2;
}
.subLinks-first span a {
    text-decoration: none;
    font-size: 15px;
    line-height: 22.5px;
    text-align: center;
    color: inherit;
}
.subLinks-first span a:last-child {
    color: rgb(0, 96, 255);
}

</style>