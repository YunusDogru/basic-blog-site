<template>
  <div class="features">
    <div class="features-content">
        <div class="features-icon">
            <Icon name="uil:graph-bar"/>
        </div>
        <h4>Creative Design</h4>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus, iure.</p>
    </div>
    <div class="features-content">
        <div class="features-icon">
            <Icon name="mingcute:fire-line"/>
        </div>
        <h4>Flexible Solutions</h4>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus, iure.</p>
    </div>
    <div class="features-content">
        <div class="features-icon">
            <Icon name="material-symbols:rocket-launch-outline"/>
        </div>
        <h4>Premium Support</h4>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus, iure.</p>
    </div>
  </div>
</template>

<script setup>

</script>

<style>

.features {
    width: 80%;
    min-height: 300px;
    padding: 30px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #fff;
    box-shadow: rgba(205, 190, 255, 0.2) 0px 8px 16px 0px;
    transform: translateY(-80px);
}
@media (max-width: 800px) {
    .features {
        flex-direction: column;
    }
    .features-content:nth-child(-n+2) {
        border-bottom: 1px solid #0060ff;
    }
}
.features-content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 15px;
}
.features-content h4 {
    font-size: 24px;
    font-weight: bold;
    margin-top: 30px;
}
.features-content p {
    color: rgb(122, 133, 149);
    font-size: 13px;
    line-height: 30px;
    margin-top: 20px;
}
.features-icon  {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
    background-color: rgba(202, 202, 202, 0.31);
    color: #0060ff;
    width: 60px;
    height: 60px;
    border-radius: 50%;
}
.features-content:hover .features-icon {
    animation: featuresIconHover 0.6s;
    animation-fill-mode: forwards;
}
@keyframes featuresIconHover {
    from {
        background-color: #fff;
        color: #0060ff;
    }
    to {
        background-color: #0060ff;
        color: #fff;
    }
}
</style>