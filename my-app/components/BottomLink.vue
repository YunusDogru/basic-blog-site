<template>
  <button @click="scrollToTop" ref="button"><Icon name="material-symbols:keyboard-arrow-up"/></button>
</template>
<style scoped>
.button {
    width: 40px;
    height: 40px;
    background-color: rgb(0, 96, 255);
    border: none;
    border-radius: 5px;
    position: fixed;
    bottom: 40px;
    right: 40px;
    color: #fff;
    font-size: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

</style>
<script setup>
const button = ref();
const handleScroll = (e) => {
    if (e.target.scrollingElement.scrollTop > 400) {
        button.value.classList.remove('scroll-button');
        button.value.classList.add('button');
    }
    else {
        button.value.classList.remove('button');
        button.value.classList.add('scroll-button');
    }
}
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

onMounted(()=>{
    window.addEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.scroll-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: none;
}
</style>