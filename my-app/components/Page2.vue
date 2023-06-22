<template>
  <section class="page2">
        <features/>
        <div class="aboutUs">
            <div class="aboutUsImg">
                <img src="http://webangon.com/html/bisness/img/about.png" alt="">
            </div>
            <div class="aboutUsContent">
                <span>ABOUT US</span>
                <h2>We are the leader of  consulting services</h2>
                <p class="pera-top">"Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam. Lorem ipsum dolor sit amet, consectetur adipisicing elit", </p>
                <p class="pera-bottom">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. </p>
                <a href="#">Hire Us</a>
            </div>
        </div>
  </section>

</template>

<script>

</script>

<style>
.page2 {
    height: auto;
    width: 100vw;
    /* min-height: 80vh; */
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    flex-direction: column;
}
.aboutUs {
    display: flex;
    align-items: flex-start;
    width: 80%;
    height: auto;
    padding-bottom: 80px;
    margin-top: 50px;
}
@media (min-width: 800px) {
    .aboutUs {
        flex-direction: row;
        top: 400px;
    }
    .aboutUsImg {
        width: 50%;
    }
    .aboutUsContent {
        width: 50%;
    }
}
@media (max-width: 800px) {
    .aboutUs {
        flex-direction: column;
        top: 900px;
    }
    .aboutUsImg {
        width: 100%;
    }
    .aboutUsContent {
        width: 100%;
    }
}
.aboutUsImg {
    display: block;
    padding: 0 15px 30px 15px;
}
.aboutUsImg img {
    width: 100%;
}
.aboutUsContent {
    padding: 0 15px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
}
.aboutUsContent span {
    color: rgb(102, 102, 102);
    font-size: 15px;
    font-weight: bold;
    margin-bottom: 20px;
}
.aboutUsContent h2 {
    font-size: 45px;
    font-weight: bold;
    margin-bottom: 30px;
}
.aboutUsContent .pera-top {
    font-size: 15px;
    font-weight: bold;
    line-height: 30px;
    background-color: rgb(244, 249, 252);
    border-left: 3px solid rgb(0, 96, 255);
    padding: 10px;
    margin-bottom: 20px;
}
.aboutUsContent .pera-bottom {
    font-size: 15px;
    line-height: 30px;
    color: rgb(122, 133, 149);
}
.aboutUsContent a {
    width: 140px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    background-color: rgb(0, 96, 255);
    color: #fff;
    text-decoration: none;
    margin-top: 50px;
}

@keyframes animation {
    from {
        height: 0;
    }
    to {
        height: fit-content;
    }
}

</style>