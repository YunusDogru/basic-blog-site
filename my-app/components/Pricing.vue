<template>
  <section class="pricing">
    <div class="pricing-header">
        <span>Our Pricing</span>
        <h2>Most Flexible Pricing</h2>
    </div>
    <div class="pricing-choices">
        <div class="choice">
            <div class="choice-top">
                <h4>Basic</h4>
            </div>
            <div class="choice-text">
                <h1>100</h1>
            </div>
            <ul class="choice-menu">
                <li>Full Support</li>
                <li>PSD Included</li>
                <li>Free Installation</li>
                <li class="remove">Free One Year Domain</li>
                <li class="remove">Unlimited Hosting Service</li>
                <li class="remove">Website Ranking</li>
            </ul>
            <div class="choice-button">
                <a href="#">Purchase</a>
            </div>
        </div>
        <div class="choice">
            <div class="choice-top">
                <h4>Advanced</h4>
            </div>
            <div class="choice-text">
                <h1>300</h1>
            </div>
            <ul class="choice-menu">
                <li>Full Support</li>
                <li>PSD Included</li>
                <li>Free Installation</li>
                <li>Free One Year Domain</li>
                <li class="remove">Unlimited Hosting Service</li>
                <li class="remove">Website Ranking</li>
            </ul>
            <div class="choice-button">
                <a href="#">Purchase</a>
            </div>
        </div>
        <div class="choice">
            <div class="choice-top">
                <h4>Pro</h4>
            </div>
            <div class="choice-text">
                <h1>500</h1>
            </div>
            <ul class="choice-menu">
                <li>Full Support</li>
                <li>PSD Included</li>
                <li>Free Installation</li>
                <li>Free One Year Domain</li>
                <li>Unlimited Hosting Service</li>
                <li>Website Ranking</li>
            </ul>
            <div class="choice-button">
                <a href="#">Purchase</a>
            </div>
        </div>
    </div>
  </section>

</template>
<script setup>


</script>
<style scoped>
.pricing {
    display: flex;
    padding: 40px 0 80px 0;
    align-items: center;
    flex-direction: column;
    width: 100%;
    background-color: rgb(244, 249, 252);
}
.pricing-header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.pricing span {
    color: rgb(102, 102, 102);
    position: absolute;
    transform: translateY(-70px);
    font-size: 15px;
}
.pricing h2 {
    font-size: 45px;
    font-weight: bold;
}
.pricing-choices {
    width: 90%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
}
.choice {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 35px 0;
    margin: 0 15px 30px 15px;
    width: 30%;
    background-color: #fff;
}
.choice:nth-child(1):hover,
.choice:nth-child(3):hover {
    animation: choiceAnim 0.2s ease-out;
    animation-fill-mode: both;
}
.choice:nth-child(1):not(:hover),
.choice:nth-child(3):not(:hover) {
    animation: choiceAnimRvrs 0.2s ease-out;
    animation-fill-mode: both;
}
.choice:nth-child(2) {
    box-shadow: rgba(0, 0, 0, 0.09) 0px 8px 16px 0px;
    transform: matrix(1, 0, 0, 1, 0, -8);
}
@keyframes choiceAnim {
    from {box-shadow: none;}
    to {box-shadow: rgba(0, 0, 0, 0.09) 0px 8px 16px 0px;transform: matrix(1, 0, 0, 1, 0, -8);}
}
@keyframes choiceAnimRvrs {
    from {box-shadow: rgba(0, 0, 0, 0.09) 0px 8px 16px 0px;transform: matrix(1, 0, 0, 1, 0, -8);}
    to {box-shadow: none;}
}
@media (max-width: 1200px) {
    .choice {
        width: 40%;
    }
}
@media (max-width: 800px) {
    .choice {
        width: 100%;
    }
}
.choice * {
    width: 100%;
    text-align: center;
}
.choice-top {
    padding-bottom: 28px;
    border-bottom: 1px solid rgb(207, 209, 252);
    font-size: 22px;
    font-weight: bold;
}
.choice-text {
    padding-top: 20px;
    font-size: 25px;
    color: rgb(0, 96, 255);
    display: flex;
    align-items: center;
    justify-content: center;
}
.choice-text h1 {
    position: relative;
    width: fit-content;
    margin: 7px;
}
.choice-text h1::before {
    content: "$";
    font-size: 20px;
    position: absolute;
    color: inherit;
    top: 0;
    left: 0;
    transform: translate(-120%, 20%);
}
.choice-menu {
    list-style: none;
    color: rgb(89, 89, 89);
    font-size: 13px;
    margin-bottom: 16px;
}
.choice-menu li{
    line-height: 20px;
    padding-bottom: 10px;
}
.remove {
    text-decoration-line: line-through;
    color: rgb(154, 154, 154) !important;
}
.choice-button {
    height: 70px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.choice-button a {
    height: 50px;
    width: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 15px;
    color: #fff;
    text-decoration: none;
    background-color: rgb(0, 96, 255);
    border-radius: 5px;
}
</style>