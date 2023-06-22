<template>
  <section class="MCAboutUs">
        <div class="header">
            <h2>Major Companies About Us</h2>
            <span>Rearrange the entire color palette, making your site unique and beatiful. Theme using a wide selection</span>
        </div>
        <div class="content">
            <div class="contentLeft">
                <img src="http://webangon.com/html/bisness/img/all/52.png">
            </div>
            <div class="contentRight">
                <div class="rightBox">
                    <div class="icon-wrapper">
                        <div class="icon"><Icon name="healthicons:city-worker-outline" class="Icon"/></div>
                    </div>
                    <div class="text">
                        <h3>Business Strategy Planning</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</p>
                    </div>
                </div>
                <div class="rightBox">
                    <div class="icon-wrapper">
                        <div class="icon"><Icon name="emojione-monotone:money-with-wings" class="Icon"/></div>
                    </div>
                    <div class="text">
                        <h3>Insurance Planning</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</p>
                    </div>
                </div>
                <div class="rightBox">
                    <div class="icon-wrapper">
                        <div class="icon"><Icon name="fa6-solid:money-bill-trend-up" class="Icon"/></div>
                    </div>
                    <div class="text">
                        <h3>Stock Market Investment</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</p>
                    </div>
                </div>
            </div>
        </div>
  </section>

</template>

<script>

</script>

<style scoped>
.MCAboutUs {
    height: auto;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
.header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    margin: 80px 0 40px 0;
}
.header span {
    color: rgb(122, 133, 149);
    line-height: 30px;
    margin-top: 15px;
    text-align: center;
    font-size: 15px;
    max-width: 500px;
}
.header h2 {
    font-size: 3rem;
    color: rgb(49,49,49);
    font-weight: bold;
}
.content {
    display: flex;
    align-items: center;
    width: 80%;
    height: auto;
    padding-bottom: 80px;
    margin-top: 50px;
}
.contentLeft,
.contentRight {
    width: 50%;
    margin: 0 15px 15px 30px;
}
@media (max-width: 800px) {
    .content {
        flex-direction: column;
    }
    .contentLeft,
    .contentRight {
        width: 100%;
    }
}
.contentLeft img {
    width: 100%;
}
.contentRight {
    padding: 30px 0 0 50px;

}
.rightBox {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.text {
    width: calc(100% - 100px);
    align-self: flex-start;
}
.text h3 {
    font-size: 22px;
    font-weight: bold;
    color: rgb(49, 49, 49);
    margin-bottom: 16px;
    text-align: left;
    line-height: 26px;
}
.text p {
    font-size: 15px;
    color: rgb(122, 133, 149);
    line-height: 28px;
    margin-bottom: 48px;
}
.icon-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 70px;
    height: 70px;
    background-color: rgb(0, 96, 255);
    border-radius: 5px;
    align-self: flex-start;

}
.icon-wrapper .icon {
    width: fit-content;
    height: fit-content;
    color: #fff;
    background-color: rgb(0, 96, 255);
}
.Icon {
    font-size: 40px !important;
}

</style>