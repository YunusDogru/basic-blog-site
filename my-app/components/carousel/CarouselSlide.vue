<template>
    <transition :name="direction" mode="in-out">
        <div v-show="visibleSlide === index" class="carousel-slide">
            <slot></slot>
        </div>
    </transition>
</template>

<script setup>

const props = defineProps({
  visibleSlide: {
    type: Number,
    required: true
  },
  index: {
    type: Number,
    required: true
  },
  direction: {
    type: String,
    required: true
  }
});
</script>

<style>
    .carousel-slide {
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
    }
    .left-enter-active {
        animation: leftInAnimation 1s ease-out;
    }
    .left-leave-active {
        animation: leftOutAnimation 1s ease-out;
    }
    @keyframes leftInAnimation {
        from {transform: translateX(100%);}
        to {transform: translateX(0);}
    }
    @keyframes leftOutAnimation {
        from {transform: translateX(0);}
        to {transform: translateX(-100%);}
    }
    .right-enter-active {
        animation: rightInAnimation 1s ease-out;
    }
    .right-leave-active {
        animation: rightOutAnimation 1s ease-out;
    }
    @keyframes rightInAnimation {
        from {transform: translateX(-100%);}
        to {transform: translateX(0);}
    }
    @keyframes rightOutAnimation {
        from {transform: translateX(0);}
        to {transform: translateX(100%);}
    }
</style>