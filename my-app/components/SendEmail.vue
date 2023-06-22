<template>

<section class="wrapper">
    <h3>You have questions?</h3>
    <form>
        <div class="personal-info">
            <input type="text" name="name" placeholder="Name" class="personal-input">
            <input type="email" name="email" placeholder="E-mail" class="personal-input">
            <input type="text" name="phone" placeholder="Phone" class="personal-input">
        </div>
        <textarea name="message" id="message" cols="30" rows="10" class="text-area" placeholder="message"></textarea>
        <a href="#">Send Mesage</a>
    </form>
</section>
</template>
<style scoped>
.wrapper {
    padding: 110px 10% 80px 10%;
    background-color: rgb(244, 249, 252);
    display: flex;
    flex-direction: column;
}
.wrapper h3 {
    color: rgb(63 63, 63);
    font-size: 1.5rem;
    font-weight: 600;
    line-height: 30px;
    margin-bottom: 50px;
    text-align: left;
}
.wrapper form {
    display: flex;
    flex-direction: column;
}
.personal-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
@media (max-width: 1200px) {
    .personal-info {
        flex-direction: column;
        width: 100%;
    }
    .personal-info input{
        width: 100% !important;
    }
}
.personal-info input,
.text-area {
    border-bottom: 1px solid rgb(224, 224, 224);
    border: none;
    border-radius: 5px;
    outline: none;
}
.personal-info input:focus,
.text-area:focus {
    border-bottom: 1px solid rgb(0, 96, 255);
}
.personal-info input {
    height: 50px;
    width: 32%;
    padding: 12px 6px;
    margin-bottom: 20px;
}
.text-area {
    padding: 20px;
    margin-bottom: 20px;
    height: 143px;
    resize: vertical;
}
.wrapper a {
    text-decoration: none;
    background-color: rgb(0, 96, 255);
    color: #fff;
    border-radius: 5px;
    margin-top: 30px;
    padding: 0 36px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: fit-content;
    height: 50px;
}

</style>