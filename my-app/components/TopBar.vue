<template>
    <section id="topbar" class="flex-center">
        <div class="container">
           <div class="contact flex-center">
             <ul>
                <li class="rightBorder" style="min-width: 215px">
                    <Icon name="uil:clock" class="contactIcon "/>
                    Mon - Sat: 09.00 - 19.00
                </li>
                <li class="rightBorder" style="min-width: 135px">
                    <a href="tel:+789675978">
                        <Icon name="mdi:phone" class="contactIcon "/>
                        +(789) 675 978
                    </a>
                </li>
                <li>
                   <a href="mailto:support@monchori.com" style="min-width: 212px">
                        <Icon name="mdi:email" class="contactIcon"/>
                        support@website.com
                   </a>
                </li>
            </ul>
           </div>
            <div class="social flex-center">
                <ul>
                    <li><Icon name="uil:facebook-f" class="socialIcon rightBorder"/></li>
                    <li><Icon name="uil:twitter" class="socialIcon rightBorder"/></li>
                    <li><Icon name="ion:logo-googleplus" class="socialIcon rightBorder"/></li>
                    <li><Icon name="mdi:pinterest" class="socialIcon rightBorder"/></li>
                    <li><Icon name="basil:linkedin-solid" class="socialIcon"/></li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
#topbar {
    width: 100vw;
    height: auto;
    min-height: 8%;
    line-height: 24px;
    font-style: normal;
    font-weight: 400;
    top: 0;
    left: 0;

}
.container {
    flex-direction: row;
    margin: 0 20px;
    width: 100%;
    display: flex;
    align-content: center;
    justify-content: space-between !important;
}
.contact {
    width: 66%;

}
.contactIcon {
    align-self: center;
    margin-right: 2px;
}
.social {
    width: 34%;

}
.social ul {
    flex-wrap: nowrap;
}

ul {
    display: flex;
    justify-content: space-around;
    align-content: center;
    flex-wrap: wrap;
}
a {
    text-decoration: none;
    cursor: pointer;
    color: rgb(189, 189, 189);
}
.contactIcon {
    color: #0060ff;
    font-size: 16px;
}
.socialIcon {
    padding: 0 4px 0 1px;
    font-size: 22px !important;
    color: rgb(189, 189, 189);
}
.socialIcon:hover {
    color: #0060ff;
    transition: 300ms;
}
.rightBorder {
    border-right: 1px solid #0060ff;

}

ul li {
    list-style-type: none;
    padding: 5px;
    color: rgb(189, 189, 189);
}
@media (max-width: 800px) {
    .container {
        flex-direction: column;
        align-items: center;
    }
    .contact ul {
        flex-direction: column;
        align-items: center;
    }
    .contact ul li {
        border: none;
    }
}
</style>