<template>
  <section class="maps">
    <div class="row1">
        <div class="maps-text">
            <h4>Contact Info:</h4>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eius- mod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris </p>
        </div>
        <ul class="maps-menu">
            <li>
                <span class="address">
                    <Icon class="contact-icon" name="ic:sharp-location-on"/>
                    Address:
                </span>
                <span class="contact-link">55, Lvabbari. Mikicuka, USA, 665087</span>
            </li>
            <li>
                <span class="address">
                    <Icon class="contact-icon" name="ic:round-local-phone"/>
                    Phone:
                </span>
                <span class="contact-link">+23 4567 890, +356 4657 8878</span>
            </li>
            <li>
                <span class="address">
                    <Icon class="contact-icon" name="ic:baseline-email"/>
                    Email:
                </span>
                <span class="contact-link">support@business.com</span>
            </li>
            <li>
                <span class="address">
                    <Icon class="contact-icon" name="material-symbols:person"/>
                    Share:
                </span>
                <span class="contact-link">
                    <Icon name="ion:social-facebook"/>
                    <Icon name="ion:social-twitter"/>
                    <Icon name="ei:sc-google-plus"/>
                    <Icon name="bxl:instagram"/>
                </span>
            </li>
        </ul>
    </div>
    <div class="row2">
        <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3651.4934239711615!2d90.38923439999999!3d23.7654375!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755b8a093137aa5%3A0x73871e0ab50f070e!2sQ98Q%2B5MH%2C%20Dhaka%201215%2C%20Banglade%C5%9F!5e0!3m2!1str!2str!4v1687438960147!5m2!1str!2str" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
  </section>
</template>

<style scoped>
.maps {
    display: flex;
    align-items: flex-start;
    justify-content: space-evenly;
    width: 100vw;
}
.row1, .row2 {
    width: 40%;
}
@media (max-width: 1000px) {
    .maps {
        flex-direction: column;
        align-items: center;
    }
    .row1, .row2 {
        width: 80%;
        margin-bottom: 40px;
    }
}
.row2 .map {
    width: 100%;
    aspect-ratio: 1/1;
}
.row1 {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-direction: column;

}
.maps-text {
    border-bottom: 1px solid rgb(204, 204, 204);
    padding-bottom: 30px;
    margin-bottom: 30px;
}
.row1 h4 {
    color: #000;
    font-size: 22px;
    font-weight: 600;
    line-height: 26px;
    margin-bottom: 30px;
    text-align: left;
}
.row1 p {
    color: rgb(122, 133, 149);
    font-size: 15px;
    line-height: 30px;
    text-align: left;
}
.maps-menu {
    list-style: none;
    display: flex;
    flex-direction: column;
    margin-bottom: 16px;
    text-align: left;
    width: 100%;
}
.maps-menu li {
    padding-bottom: 15px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.address{
    color: rgb(89, 89, 89);
    font-size: 14px;
    font-weight: 600;
}
.contact-icon {
    font-size: 16px;
    margin-right: 25px;

}
.contact-link {
    font-size: 15px;
    color: rgb(89, 89, 89);
}
.contact-link:last-child *{
    font-size: 16px;
    margin-left: 30px;
    cursor: pointer;
}
</style>