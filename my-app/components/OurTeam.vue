<template>
  <section class="our-team">
    <div class="team-header">
        <span>Our Team</span>
        <h2>People Behind Success</h2>
    </div>
    <div class="team-content">
        <div class="team-member-box">
            <img src="http://webangon.com/html/bisness/img/team/team1.jpg" class="team-member-img">
            <div class="team-member-text">
                <h4>Michael Redux</h4>
                <span>creative builder</span>
                <div class="team-member-icons">
                    <a href="#"><Icon name="gg:facebook"/></a>
                    <a href="#"><Icon name="gg:twitter"/></a>
                    <a href="#"><Icon name="gg:google"/></a>
                    <a href="#"><Icon name="gg:instagram"/></a>
                </div>
            </div>
        </div>
        <div class="team-member-box">
            <img src="http://webangon.com/html/bisness/img/team/team2.jpg" class="team-member-img">
            <div class="team-member-text">
                <h4>Michael Redux</h4>
                <span>creative builder</span>
                <div class="team-member-icons">
                    <a href="#"><Icon name="gg:facebook"/></a>
                    <a href="#"><Icon name="gg:twitter"/></a>
                    <a href="#"><Icon name="gg:google"/></a>
                    <a href="#"><Icon name="gg:instagram"/></a>
                </div>
            </div>
        </div>
        <div class="team-member-box">
            <img src="http://webangon.com/html/bisness/img/team/team3.jpg" class="team-member-img">
            <div class="team-member-text">
                <h4>Michael Redux</h4>
                <span>creative builder</span>
                <div class="team-member-icons">
                    <a href="#"><Icon name="gg:facebook"/></a>
                    <a href="#"><Icon name="gg:twitter"/></a>
                    <a href="#"><Icon name="gg:google"/></a>
                    <a href="#"><Icon name="gg:instagram"/></a>
                </div>
            </div>
        </div>
        <div class="team-member-box">
            <img src="http://webangon.com/html/bisness/img/team/team3.jpg" class="team-member-img">
            <div class="team-member-text">
                <h4>Michael Redux</h4>
                <span>creative builder</span>
                <div class="team-member-icons">
                    <a href="#"><Icon name="gg:facebook"/></a>
                    <a href="#"><Icon name="gg:twitter"/></a>
                    <a href="#"><Icon name="gg:google"/></a>
                    <a href="#"><Icon name="gg:instagram"/></a>
                </div>
            </div>
        </div>
        <div class="team-member-box">
            <img src="http://webangon.com/html/bisness/img/team/team4.jpg" class="team-member-img">
            <div class="team-member-text">
                <h4>Michael Redux</h4>
                <span>creative builder</span>
                <div class="team-member-icons">
                    <a href="#"><Icon name="gg:facebook"/></a>
                    <a href="#"><Icon name="gg:twitter"/></a>
                    <a href="#"><Icon name="gg:google"/></a>
                    <a href="#"><Icon name="gg:instagram"/></a>
                </div>
            </div>
        </div>
        <div class="team-member-box">
            <img src="http://webangon.com/html/bisness/img/team/team1.jpg" class="team-member-img">
            <div class="team-member-text">
                <h4>Michael Redux</h4>
                <span>creative builder</span>
                <div class="team-member-icons">
                    <a href="#"><Icon name="gg:facebook"/></a>
                    <a href="#"><Icon name="gg:twitter"/></a>
                    <a href="#"><Icon name="gg:google"/></a>
                    <a href="#"><Icon name="gg:instagram"/></a>
                </div>
            </div>
        </div>
    </div>
  </section>

</template>

<script setup>


</script>

<style scoped>
.our-team {
    display: flex;
    padding: 40px 0;
    align-items: center;
    flex-direction: column;
    width: 100%;
}
.team-header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.team-header span {
    color: rgb(102, 102, 102);
    position: absolute;
    transform: translateY(-50px);
    font-size: 15px;
}
.team-header h2 {
    font-size: 32px;
    font-weight: bold;
}
.team-content {
    width: 80%;
    height: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;    
}
.team-member-box {
    width: 30%;
    margin-bottom: 30px;
    background-color: #fff;
    height: fit-content;
    display: flex;
    position: relative;
    text-align: center;
    line-height: 25px;
}
@media (max-width: 800px) {
    .team-member-box {
        width: 100%;
    }
}
.team-member-img {
    width: 100%;
}
.team-member-text {
    opacity: 0;
    transition: all 0.4s ease;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    color: #fff;
    text-align: center;
}
.team-member-text h4 {
    font-size: 22px;
    font-weight: bold;
    margin-bottom: 20px;
}
.team-member-text span {
    font-size: 15px;
}
.team-member-icons {
    margin-top: 20px;
    display: flex;
    align-items: center;
    justify-content: space-around;
}
.team-member-icons a {
    width: 36px;
    height: 36px;
    cursor: pointer;
    text-decoration: none;
    color: #fff;
}
.team-member-box:hover::before{
    content: "";
    position: absolute;
    top: 0;
    width: 100%;
    background-color: rgb(0, 96, 255);
    animation: teamFadeIn 0.5s ease;
    animation-fill-mode: forwards;
    z-index: 3;
}
@keyframes teamFadeIn {
    from {
        opacity: 0;
        height: 0;
    }
    to {
        opacity: 1;
        height: 100%;
    }
}
.team-member-box:not(:hover)::before{
    content: "";
    position: absolute;
    bottom: 0;
    width: 100%;
    background-color: rgb(0, 96, 255);
    animation: teamFadeOut 0.5s ease;
    animation-fill-mode: forwards;
}
@keyframes teamFadeOut {
    from {
        opacity: 1;
        height: 100%;
    }
    to {
        opacity: 0;
        height: 0;
    }
}
.team-member-box:hover .team-member-text {
    opacity: 1;
    z-index: 5;
}
</style>