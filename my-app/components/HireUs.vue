<template>
  <section class="hire-us">
    <div class="hire-us-left">
        <span>ABOUT US</span>
        <h2>We are the leader of finance consulting services</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam. Lorem ipsum dolor sit amet, consectetur adipisicing elit, </p>
        <ul class="about-features">
            <li>
                <Icon name="mdi:check-bold" class="check"/>
                We Have Best Market Analysis
            </li>
            <li>
                <Icon name="mdi:check-bold" class="check"/>
                We Provide Strong Management
            </li>
            <li>
                <Icon name="mdi:check-bold" class="check"/>
                The Best Finance Facilities
            </li>
        </ul>
        <a href="#">Hire Us</a>
    </div>
    <div class="hire-us-right">
        <div class="column1 column">
            <div class="feature-box">
                <Icon name="streamline:money-graph-bar-increase-up-product-performance-increase-arrow-graph-business-chart" class="feature-box-icon"/>
                <h3>Business are best Solution</h3>
            </div>
            <div class="feature-box">
                <Icon name="streamline:money-cash-search-dollar-search-pay-product-currency-query-magnifying-cash-business-money-glass" class="feature-box-icon"/>
                <h3>Financial of our Consultation</h3>
            </div>
        </div>
        <div class="column2 column">
            <div class="feature-box">
                <Icon name="ph:coins-light" class="feature-box-icon"/>
                <h3>Marketing and our Strategy</h3>
            </div>
            <div class="feature-box">
                <Icon name="ph:coins-light" class="feature-box-icon"/>
                <h3>Marketing and our Strategy</h3>
            </div>
        </div>
    </div>
  </section>
</template>
<style scoped>
.hire-us {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    height: auto;
    padding: 110px 10% 80px 10%;
}
.hire-us-left,
.hire-us-right {
    width: 50%;
    margin: 0 15px;
    padding: 0 0 30px 20px;
    display: flex;
}
@media (max-width: 1000px) {
    .hire-us {
        flex-direction: column;
    }
    .hire-us-left,
    .hire-us-right {
        width: 100%;
    }
}

.hire-us-left {
    align-items: flex-start;
    flex-direction: column;
}
.hire-us-left span {
    margin-bottom: 20px;
    color: rgb(102, 102, 102);
    font-size: 15px;
    letter-spacing: 1x;
    line-height: 22.5px;
    text-align: left;
    height: fit-content;

}
.hire-us-left h2 {
    font-size: 2.5rem;
    color: #000000;
    font-weight: 700;
    line-height: 3.5rem;
    text-align: left;
    margin-bottom: 30px;
}
.hire-us-left p {
    color: rgb(122, 133, 149);
    font-size: 13px;
    font-weight: 500;
    line-height: 30px;
    text-align: left;
    padding-right: 15px;
}
.hire-us-left ul {
    color: rgb(33, 37, 41);
    font-size: 16px;
    list-style: none;
    line-height: 24px;
    margin-top: 30px;
    display: flex;
    flex-direction: column;
}
.hire-us-left ul li {
    font-size: 18px;
    font-weight: 600;
    line-height: 22px;
    margin-bottom: 22px;
}
.check {
    font-size: 18px;
    color: rgb(0, 96, 255);
    text-align: left;
}
.hire-us-left a {
    text-decoration: none;
    background-color: rgb(0, 96, 255);
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    width: 130px;
    height: 50px;
    margin-top: 30px;
}
.hire-us-right {
    flex-direction: row;
}
.hire-us-right .column {
    display: flex;
    flex-direction: column;
    height: auto;
    width: 50%;
}
.hire-us-right .column1 {
    align-self: flex-start;
    margin-right: 15px;
}
.hire-us-right .column2 {
    align-self: flex-end;
    margin-top: 50px;
}
@media (max-width: 800px) {
    .hire-us-right {
        flex-direction: column;
    }
    .column {
        width: 100% !important;
    }
    .column2 {
        margin-top: 15px !important;
    }
}
.feature-box {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-direction: column;
    padding: 30px;
    box-shadow: rgba(205, 190, 255, 0.2) 0px 8px 16px 0px;
}
.feature-box:hover {
    animation: boxShadow 0.3s ease-out;
    animation-fill-mode: forwards;
}
@keyframes boxShadow {
    to {
        box-shadow: rgba(0, 0, 0, 0.3) 0px 10px 40px -10px;
    }
}
.feature-box .feature-box-icon {
    color: rgb(0, 96, 255);
    font-size: 40px;
    margin: 10px 0;
}
.feature-box h3 {
    color: #000000;
    font-size: 20x;
    font-weight: 600;
    line-height: 32px;
    margin: 10px 0 8px 0;
    text-align: left;
}
</style>