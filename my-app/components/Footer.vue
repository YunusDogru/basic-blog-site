<template>
  <section class="footer">
    <div class="footer-top-area">
        <div class="footer-top1 footer-top-content">
            <img src="http://webangon.com/html/bisness/img/logo/logo%20(3).png">
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit, sed do eiusmod teminc.</p>
            <form class="newsletter-form">
                <input type="email" class="input-email" placeholder="Your email..">
                <button type="submit"><Icon name="ion:md-mail"/></button>
            </form>
        </div>
        <div class="footer-top2 footer-top-content">
            <h4 class="footer-text">Usefull links</h4>
            <ul class="footer-links">
                <li>
                    <div class="links-img">
                        <a href="#"><img src="http://webangon.com/html/bisness/img/img-1.jpg"></a>
                    </div>
                    <div class="links-info">
                        <h4><a href="#">How to Improve Your Sales Volume </a></h4>
                        <span>24th Aug 2019</span>
                    </div>
                </li>
                <li>
                    <div class="links-img">
                        <a href="#"><img src="http://webangon.com/html/bisness/img/img-1.jpg"></a>
                    </div>
                    <div class="links-info">
                        <h4><a href="#">How to Improve Your Sales Volume </a></h4>
                        <span>24th Aug 2019</span>
                    </div>
                </li>
            </ul>
        </div>
        <div class="footer-top3 footer-top-content">
            <h4 class="footer-text">Contact Us</h4>
            <ul class="footer-menu">
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Home
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    About us
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Services
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Policy
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Work
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Blogs
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Contact
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Support
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Career
                </li>
                <li>
                    <a href="#">
                        <Icon class="footer-icon" name="ant-design:caret-right-filled"/>
                    </a>
                    Privacy
                </li>
            </ul>
        </div>
        <div class="footer-top4 footer-top-content">
            <h4 class="footer-text">Instagram</h4>
            <ul class="footer-insta">
                <li v-for="i in [1,2,3,4,5,6]" :key="i">
                    <a href="#"><img :src="`http://webangon.com/html/bisness/img/all/ins${i}.jpg`"></a>
                </li>
            </ul>
        </div>
    </div>
    <div class="footer-bottom-area">
        <div class="copyright">
            <p>Copyright ©2022 </p>
            <a href="https://codecanyon.net/user/themexhunter">ThemexHunter</a>
            . All Rights Reserved
        </div>
        <div class="footer-social-icon">
            <a href="#">
                <Icon name="bx:bxl-facebook"/>
            </a>
            <a href="#">
                <Icon name="bx:bxl-twitter"/>
            </a>
            <a href="#">
                <Icon name="bx:bxl-google"/>
            </a>
            <a href="#">
                <Icon name="bx:bxl-instagram"/>
            </a>
            <a href="#">
                <Icon name="bx:bxl-linkedin"/>
            </a>
            <a href="#">
                <Icon name="bx:bxl-pinterest"/>
            </a>
        </div>
    </div>
  </section>
</template>
<style scoped>
.footer-bottom-area {
    background-color: rgb(0, 96, 255);
    font-size: 16px;
    font-weight: 500;
    line-height: 24px;
    padding: 22px 10%;
    text-align: left;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
@media (max-width: 800px) {
    .footer-bottom-area {
        flex-direction: column;
        justify-content: center;
    }
    .copyright,
    .footer-social-icon {
        width: fit-content;
        flex-wrap: wrap;
    }
}
.copyright,
.footer-social-icon {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row;
}
.copyright {
    margin: 10px 0;
    color: #fff;
}
.copyright a {
    margin: 0 3px;
    color: #fff;
}
.copyright a:hover {
    text-decoration: underline;
}
.footer-social-icon a {
    margin-right: 20px;
    font-size: 18px;
    color: #fff;
}
.footer {
    width: 100vw;
    background-color: #000000;
}
.footer-top-area {
    width: 100%;
    padding: 110px 80px 80px 80px;
    display: flex;
    justify-content: flex-start;
    position: relative;
}
.footer-top-area::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    background-image: url("http://webangon.com/html/bisness/img/footer-bg.png");
}
.footer-top-content {
    width: 25%;
    margin: 0 15px;
    align-self: flex-start;
    z-index: 3;
    margin-bottom: 30px;
}
@media (max-width: 1100px) {
    .footer-top-area {
        flex-wrap: wrap;
    }
    .footer-top-content {
        width: 40%;
    }
}
@media (max-width: 800px) {
    .footer-top-content:nth-child(-n+2) {
        width: 100%;
    }
}
@media (max-width: 650px) {
    .footer-top-content {
        width: 100%;
    }
}
.footer-top1 {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;
}
.footer-top1 img {
    max-width: 100%;
}
.footer-top1 p {
    color: rgb(204,204,204);
    font-size: 15px;
    line-height: 30px;
    text-align: left;
}
.newsletter-form {
    padding-top: 30px;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
}
.newsletter-form .input-email {
    height: 45px;
    width: 60%;
    padding: 15px 6px;
    border: 1px solid rgb(73, 80, 87);
    background-color: #fff;
    box-shadow: rgba(0,0,0,0.05) 0px 5px 7px 0px;
    color: rgb(73, 80, 87);
    font-size: 13px;
    text-align: start;
}
.input-email:focus {
    outline: none;
}
.newsletter-form button {
    width: 45px;
    height: 45px;
    background-color: rgb(0, 96, 255);
    border: 1px solid rgb(73, 80, 87);
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    border: none;
}
.footer-top2 {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;
}
.footer-text {
    margin-bottom: 25px;
    color: #fff;
    font-size: 22px;
    font-weight: 600;
    line-height: 25px;
    text-align: left;
}
.footer-links {
    color: rgb(33, 37, 41);
    font-size: 16px;
    line-height: 24px;
    text-align: left;
    list-style: none;
}
.footer-links li {
    margin-bottom: 24px;
    list-style: none;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
}
.links-img {
    margin-right: 20px;
    text-align: left;
}
.links-info {
    font-size: 15px;
    font-weight: 600;
    line-height: 22.5px;
    margin-bottom: 4pxx;
    text-align: left;
}
.links-info h4{
    font-size: 15px;
    font-weight: 600;
    margin-bottom: 4px;
    text-align: left;
}
.links-info h4 a {
    text-decoration: none;
    transition: color 0.3s;
    color: #fff;
}
.links-info h4 a:hover {
    color: rgb(0, 96, 255) !important;
}
.links-info span {
    color: rgb(204,204,204);
    font-size: 12px;
    display: inline-block;
    line-height: 18px;
}
.footer-menu {
    list-style: none;
    width: 100%;
    padding-right: 20px;
    margin-bottom: 16px;
}
.footer-menu li {
    width: 50%;
    display: inline-block;
    color: rgb(204,204,204);
    padding-bottom: 10px;
    transition: color 0.2s ease-out;
}
.footer-menu li a {
    text-decoration: none;
    color: rgb(204,204,204);
    display: inline-block;
    font-size: 15px;
}
.footer-menu li:hover {
    animation: footerLinkAnim 0.2s ease-out;
    animation-fill-mode: forwards;
    color: rgb(0, 96, 255) !important;
}
@keyframes footerLinkAnim {
    to {
        transform: translateX(10px);
    }
}
.footer-icon {
    font-size: 10px;
    color: inherit;
}
.footer-insta {
    width: 100%;
    margin-top: 10px;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    transition: color 0.3s ease-out;
}
.footer-menu li:hover .footer-icon{
    color: rgb(0, 96, 255)
}
.footer-insta li {
    width: 30%;
    margin-bottom: 22px;
}
.footer-insta li img {
    max-width: 100%;
}
</style>