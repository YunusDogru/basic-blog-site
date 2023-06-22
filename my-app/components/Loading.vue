<template>
  <section class="loading" ref="loading">
    <div class="loading-icon">
        <span class="span1"></span>
        <span class="span2"></span>
        <span class="span3"></span>
        <span class="span4"></span>
        <span class="span5"></span>
  </div>
  </section>
</template>
<script setup>
const loading = ref();

onMounted(()=>{
    setTimeout(()=>{
        loading.value.classList.add('disappear')
    },1000)
})
</script>
<style scoped>
.disappear {
    display: none !important;
}
.loading {
    width: 100vw;
    height: 100vh;
    position: relative;
    background-color: #fff;
    animation-name: disappear;
    animation-fill-mode: forwards;
}
.loading-icon {
    position: absolute;
    display: flex;
    align-items: center;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.loading-icon span {
    width: 10px;
    margin-right: 3px;
    height: 5px;
    background-color: rgb(0, 96, 255);
}
.span1 {
    animation: growUp 0.5s ease-out;
    animation-delay: 0.2s;
    animation-fill-mode: forwards;
}
.span2 {
    animation: growUp 0.5s ease-out;
    animation-delay: 0.35s;
    animation-fill-mode: forwards;
}
.span3 {
    animation: growUp 0.5s ease-out;
    animation-delay: 0.5s;
    animation-fill-mode: forwards;
}
.span4 {
    animation: growUp 0.5s ease-out;
    animation-delay: 0.65s;
    animation-fill-mode: forwards;
}
.span5 {
    animation: growUp 0.5s ease-out;
    animation-delay: 0.8s;
    animation-fill-mode: forwards;
}

@keyframes growUp {
    0% {
        opacity: 0.5;
        height: 5px;
    }
    50% {
        opacity: 1;
        height: 35px;
    }
    100% {
        opacity: 0.5;
        height: 5px;
    }
}
</style>