<template>
  <section class="contact-us2">
    <div class="contact-header">
        <span>Contact</span>
        <h2>Contact Us</h2>
    </div>
    <div class="contact-bottom">
        <div class="contact-content">
            <div class="contact-icon">
                <Icon name="ph:envelope-simple-open"/>
            </div>
            <h4>Our Mail Here</h4>
            <p>Admin@ThemeXHunter.com<br>Info@XLDevelopment.com</p>
        </div>
        <div class="contact-content">
            <div class="contact-icon">
                <Icon name="geo:ui-earth-west"/>
            </div>
            <h4>Visit Our Site</h4>
            <p>27 Division St, New York, NY <br>10002, Jaklina, United Kingpung</p>
        </div>
        <div class="contact-content">
            <div class="contact-icon">
                <Icon name="streamline:interface-help-customer-support-1-customer-headset-help-microphone-phone-support"/>
            </div>
            <h4>Call To Us</h4>
            <p>+8 (123) 985 789 <br>+787 878897 87</p>
        </div>
    </div>
  </section>

</template>

<style scoped>
.contact-us2 {
    display: flex;
    padding: 40px 0;
    align-items: center;
    flex-direction: column;
    width: 100%;
}
.contact-header {
    height: 200px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.contact-header span {
    color: rgb(102, 102, 102);
    font-size: 15px;
}
.contact-header h2 {
    font-size: 2rem;
    font-weight: bold;
}
.contact-bottom {
    width: 80%;
    min-height: 300px;
    padding: 30px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #fff;
    box-shadow: rgba(205, 190, 255, 0.2) 0px 8px 16px 0px;
    background-color: rgb(244, 249, 252);

}
@media (max-width: 800px) {
    .contact-bottom {
        flex-direction: column;
        width: 100%;
    }
    .contact-content:nth-child(-n+2) {
        border-bottom: 1px solid #0060ff;
    }
}
.contact-content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 15px;
    width: calc(100% / 3);
}
@media (max-width: 1000px) {
    .contact-bottom {
        flex-wrap: wrap;
    }
    .contact-content {
        width: 50%;
    }
}
.contact-content h4 {
    font-size: 24px;
    font-weight: bold;
    margin-top: 30px;
}
.contact-content p {
    color: rgb(122, 133, 149);
    font-size: 15px;
    line-height: 30px;
    font-weight: 500;
    margin-top: 20px;
}
.contact-icon  {
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
.contact-content:hover .contact-icon {
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