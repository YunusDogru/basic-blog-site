<template>
  <section class="services">
    <div class="services-header">
        <span>Services</span>
        <h2>What We Offer</h2>
    </div>
    <div class="services-content">
        <div class="content-box">
            <Icon class="servicesIconTop" name="fa6-brands:dochub"/>
            <h3>Bussiness Plan</h3>
            <p>Et harum quidem rerum facilis est et expe dita dis tinctio. Nam libero tempore.</p>
            <Icon class="servicesIconBottom" name="material-symbols:arrow-circle-right-outline"/>
        </div>
        <div class="content-box">
            <Icon class="servicesIconTop" name="uil:graph-bar"/>
            <h3>Creative Solutions</h3>
            <p>Et harum quidem rerum facilis est et expe dita dis tinctio. Nam libero tempore.</p>
            <Icon class="servicesIconBottom" name="material-symbols:arrow-circle-right-outline"/>
        </div>
        <div class="content-box">
            <Icon class="servicesIconTop" name="mingcute:fire-line"/>
            <h3>Websites Rank</h3>
            <p>Et harum quidem rerum facilis est et expe dita dis tinctio. Nam libero tempore.</p>
            <Icon class="servicesIconBottom" name="material-symbols:arrow-circle-right-outline"/>
        </div>
        <div class="content-box">
            <Icon class="servicesIconTop" name="gg:briefcase"/>
            <h3>SEO Marketing</h3>
            <p>Et harum quidem rerum facilis est et expe dita dis tinctio. Nam libero tempore.</p>
            <Icon class="servicesIconBottom" name="material-symbols:arrow-circle-right-outline"/>
        </div>
        <div class="content-box">
            <Icon class="servicesIconTop" name="material-symbols:rocket-launch-outline"/>
            <h3>Financing Solutions</h3>
            <p>Et harum quidem rerum facilis est et expe dita dis tinctio. Nam libero tempore.</p>
            <Icon class="servicesIconBottom" name="material-symbols:arrow-circle-right-outline"/>
        </div>
        <div class="content-box">
            <Icon class="servicesIconTop" name="simple-icons:chromecast"/>
            <h3>Could Computing</h3>
            <p>Et harum quidem rerum facilis est et expe dita dis tinctio. Nam libero tempore.</p>
            <Icon class="servicesIconBottom" name="material-symbols:arrow-circle-right-outline"/>
        </div>
    </div>
  </section>

</template>

<script setup>


</script>

<style scoped>
.services {
    background-color: rgb(244, 249, 252);
    display: flex;
    align-items: center;
    flex-direction: column;
    width: 100%;
}
.services-header {
    height: 250px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.services-header span {
    color: rgb(102, 102, 102);
    position: absolute;
    transform: translateY(-50px);
    font-size: 15px;
}
.services-header h2 {
    font-size: 3rem;
    font-weight: bold;
}
.services-content {
    width: 80%;
    height: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;    
}
.content-box {
    width: 30%;
    background-color: #fff;
    height: 400px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    padding: 30px 30px;
    margin: 0 10px 40px 10px;
    text-align: center;
    line-height: 25px;
    box-shadow: rgba(171, 171, 171, 0.1) 0px 15px 44px 0px;
}
.content-box:hover {
    background-image: url("http://webangon.com/html/bisness/img/s2.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    animation: contentBoxNormal 0.5s ease;
    animation-fill-mode: forwards;
}
@media (max-width: 1200px) {
    .content-box {
        height: 550px;
    }
}
@media (max-width: 800px) {
    .content-box {
        height: auto;
        width: 100%;
    }
    .content-box:hover {
        animation: contentBoxMobile 0.5s ease;
        animation-fill-mode: forwards;
    }
}
@keyframes contentBoxMobile {
    from {
        background-position: top;
    }
    to {
        background-position: center;
    }
}
@keyframes contentBoxNormal {
    from {
        background-position: left;
    }
    to {
        background-position: center;
    }
}
.content-box:hover h3,
.content-box:hover p {
    color: #fff !important;
}
.servicesIconTop {
    font-size: 30px;
    color: rgb(0, 96, 255);
    margin: 5px 0 20px 0;
}
.content-box h3 {
    font-size: 22px;
    font-weight: bold;
    padding-top: 7px;
    margin-bottom: 8px;
}
.content-box p {
    color: rgb(122, 133, 149);
    padding-top: 15px;
    font-size: 15px;
}
.servicesIconBottom {
    font-size: 30px;
    color: rgb(0, 96, 255);
    margin-top: 20px;
}
</style>