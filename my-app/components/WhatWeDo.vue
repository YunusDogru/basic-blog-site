<template>
  <section class="what-we-do">
    <div class="header">
        <h2>What We Do?</h2>
        <span>Rearrange the entire color palette, making your site unique and beautiful.theme using a wide selection</span>
    </div>
    <div class="content">
        <div class="content-box">
            <Icon class="box-icon" name="ph:coins-light"></Icon>
            <div class="box-text">
                <h4>Technology Advising</h4>
                <p>Seddo eiusmod tempor incididunt labore lore magna aliqua uisipsum suspendis incididun se ultrices gravide.</p>
            </div>
        </div>
        <div class="content-box">
            <Icon class="box-icon" name="bi:bar-chart"></Icon>
            <div class="box-text">
                <h4>Financial Consulting</h4>
                <p>Seddo eiusmod tempor incididunt labore lore magna aliqua uisipsum suspendis incididun se ultrices gravide.</p>
            </div>
        </div>
        <div class="content-box">
            <Icon class="box-icon" name="nimbus:fire"></Icon>
            <div class="box-text">
                <h4>Business Strategy</h4>
                <p>Seddo eiusmod tempor incididunt labore lore magna aliqua uisipsum suspendis incididun se ultrices gravide.</p>
            </div>
        </div>
        <div class="content-box">
            <Icon class="box-icon" name="ph:briefcase"></Icon>
            <div class="box-text">
                <h4>Planning & Conducting</h4>
                <p>Seddo eiusmod tempor incididunt labore lore magna aliqua uisipsum suspendis incididun se ultrices gravide.</p>
            </div>
        </div>
        <div class="content-box">
            <Icon class="box-icon" name="octicon:rocket-16"></Icon>
            <div class="box-text">
                <h4>Financial Opportunities</h4>
                <p>Seddo eiusmod tempor incididunt labore lore magna aliqua uisipsum suspendis incididun se ultrices gravide.</p>
            </div>
        </div>
        <div class="content-box">
            <Icon class="box-icon" name="simple-icons:chromecast"></Icon>
            <div class="box-text">
                <h4>Creative Best Solutions</h4>
                <p>Seddo eiusmod tempor incididunt labore lore magna aliqua uisipsum suspendis incididun se ultrices gravide.</p>
            </div>
        </div>
    </div>
  </section>

</template>

<script setup>


</script>

<style scoped>
.what-we-do {
    display: flex;
    padding: 40px 0;
    align-items: center;
    flex-direction: column;
    width: 100%;
    background-color: rgb(244, 249, 252);
}
.header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.header span {
    color: rgb(102, 102, 102);
    font-size: 15px;
    max-width: 500px;
    line-height: 30px;
}
.header h2 {
    font-size: 3rem;
    font-weight: bold;
}
.content {
    width: 80%;
    height: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;    
}
.content-box {
    width: calc(50% - 30px);
    margin: 0 15px 30px 15px;
    padding: 40px;
    border-radius: 10px;
    background-color: #fff;
    height: fit-content;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
}
@media (max-width: 800px) {
    .content-box {
        width: 100%;
    }

}
.box-icon {
    font-size: 80px;
    min-width: 40px;
    height: 40px;
    color: rgb(0, 96, 255);
}
.box-text {
    color: #fff;
    text-align: left;
    padding-left: 28px;
}
.box-text h4 {
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 20px;
    position: relative;
    color: #000;
}
.box-text h4::before {
    content: "";
    background-color: rgb(244, 249, 252);
    position: absolute;
    bottom: -17px;
    left: 0;
    cursor: pointer;
    height: 3px;
    width: 120px;
}
.content-box:hover h4::after{
    content: "";
    background-color: rgb(0, 96, 255);
    position: absolute;
    bottom: -17px;
    left: 0;
    cursor: pointer;
    height: 3px;
    animation: stickAnim 0.3s ease-out;
    animation-fill-mode: forwards;
}
@keyframes stickAnim {
    from {width: 0; opacity: 0;}
    to {width: 120px; opacity: 1;}
}
.box-text p {
    font-size: 13px;
    color: rgb(122, 133, 149) !important;
    line-height: 30px;
    text-align: left;
}

</style>