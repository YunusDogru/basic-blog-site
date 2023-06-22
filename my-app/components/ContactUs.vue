<template>
  <section class="contactUs">
    <div class="contact-wrapper">
        <div class="comment-respond">
            <form class="clearfix">
                <textarea class="text-area" placeholder="write.."></textarea>
                <div class="name-inputs">
                    <input type="text" class="input-firstname" placeholder="First Name..">
                    <input type="text" class="input-lastname" placeholder="Last Name..">
                </div>
                <input type="email" class="input-email" placeholder="Email Address..">
                <button type="submit" class="input-submit">Send Message</button>
            </form>
        </div>
        <div class="contact-content">
            <span>CONTACT US</span>
            <h2>Request a call back Appointment?</h2>
            <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat,
                sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
                Lorem ipsum dolor sit amet, consetetur sadipscing elitr.
            </p>
            <a href="#">Appointment</a>
        </div>
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
.contactUs {
    min-height: 100vh;
    background-image: url("http://webangon.com/html/bisness/img/all/inner.jpg");;
    background-size: cover;
    background-attachment: fixed;
    position: relative;
    padding: 110px 0 80px 0;
    display: flex;
    justify-content: center;
    align-items: center;
}
.contactUs::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    background-color: rgba(0,0,0,0.4);
}
.contact-wrapper {
    padding: 0 15px;
    width: 80%;
    z-index: 3;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.comment-respond {
    width: 50%;
    margin: 0 15px 30px 15px;
    padding: 50px;
    background-color: #fff;
    border-radius: 5px;
}
.clearfix {
    width: 100%;
    height: 100%;
}
.clearfix * {
    border-radius: 5px;
    color: #000000;
    font-size: 15px;
    line-height: 24px;
    display: flex;
}
.clearfix:last-child {
    border: none;
    padding: none;
    color: #fff;
}
.text-area {
    width: 100%;
    min-height: 200px;
    margin-bottom: 20px;
    padding: 6px 15px;
    border: 1px solid rgb(230, 233, 236);
    resize: vertical;
}
.name-inputs {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0;
    margin-bottom: 20px;
}
.input-firstname {
    height: 50px;
    width: 45%;
    padding: 6px 15px;
    border: 1px solid rgb(230, 233, 236);
}
.input-lastname {
    height: 50px;
    width: 45%;
    padding: 6px 15px;
    border: 1px solid rgb(230, 233, 236);
}
.input-email {
    height: 50px;
    padding: 6px 15px;
    width: 100%;
    margin-bottom: 20px;
    border: 1px solid rgb(230, 233, 236);
}
.input-submit {
    height: 50px;
    width: 100%;
    background-color: rgb(0, 96, 255);
    border: none;
    outline: none;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
}

.contact-content {
    width: 50%;
    margin: 0 15px 30px 15px;
    padding-top: 30px;
    border-radius: 5px;
    color: #fff;
    display: flex;
    flex-direction: column;
}
.contact-content span {
    font-size: 16px;
    font-weight: 600;
    margin-bottom: 22px;
}
.contact-content h2 {
    margin-top: 20px;
    font-size: 45px;
    font-weight: 700;
    line-height: 45px;
    text-align: left;
    text-transform: capitalize;
} 
.contact-content p {
    margin-top: 26px;
    color: rgb(215, 216, 228);
    font-size: 15px;
    font-weight: 500;
    line-height: 30px;
    text-align: left;
}
.contact-content a {
    margin-top: 40px;
    width: 180px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    background-color: rgb(0, 96, 255);
    color: #fff;
    text-decoration: none;
}
@media (max-width: 1000px) {
    .name-inputs {
        flex-direction: column;
        margin: 0;
    }
    .input-firstname,
    .input-lastname {
        width: 100%;
        margin-bottom: 20px;
    }
}
@media (max-width: 800px) {
    .contact-wrapper {
        flex-direction: column;
    }
    .contact-wrapper *{
        width: 100%;
    }
}
</style>