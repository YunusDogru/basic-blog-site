
<script setup>

const navbar = ref();

const navbarActiveLinks = reactive({
    isHamburgerActive: false,
    isHomeActive: false,
    isServiceActive: false,
    isPagesActive: false,
    isBlogActive: false
})
const handleScroll = (e) => {
    if (e.target.scrollingElement.scrollTop > 400) {
        navbar.value.classList.add('sticky');
    }
    else {
        navbar.value.classList.remove('sticky');
    }
}
onMounted(()=>{
    window.addEventListener('scroll', handleScroll)
})
</script>


<template>
    <section class="navbar" ref="navbar" @click="scroll">
        <div class="mobileButtons">
            <NuxtLink class="logo" to="/">
                <img src="http://webangon.com/html/bisness/img/logo/logo%20(3).png" alt="">
            </NuxtLink>
            <button class="hamburger-button" @click="navbarActiveLinks.isHamburgerActive = !navbarActiveLinks.isHamburgerActive">MENU <Icon name="icon-park-outline:hamburger-button" class="hamburger-icon"/></button>
        </div>
       <ul :class="[{'hamburger-active': navbarActiveLinks.isHamburgerActive}, 'links']">
            <li class="link" @click="navbarActiveLinks.isHomeActive = !navbarActiveLinks.isHomeActive">
                <NuxtLink to="/">Home<Icon name="material-symbols:keyboard-arrow-down"/></NuxtLink>
                <div :class="[{'home-active': navbarActiveLinks.isHomeActive}, 'dropdownlinks']">
                    <NuxtLink to="/">Home Page 1</NuxtLink>
                    <NuxtLink to="/">Home Page 2</NuxtLink>
                    <NuxtLink to="/">Home Page 3</NuxtLink>
                    <NuxtLink to="/">Home Page 4</NuxtLink>
                    <NuxtLink to="/">Home Page 5</NuxtLink>
                    <NuxtLink to="/">Home Page 6</NuxtLink>
                </div>
            </li>
            <li class="link">
                <NuxtLink to="/aboutus">About Us</NuxtLink>
            </li>
            <li class="link" @click="navbarActiveLinks.isServiceActive = !navbarActiveLinks.isServiceActive">
                <NuxtLink to="/service">Service<Icon name="material-symbols:keyboard-arrow-down"/></NuxtLink>
                <div :class="[{'service-active': navbarActiveLinks.isServiceActive}, 'dropdownlinks']">
                    <NuxtLink to="/service">Service One</NuxtLink>
                    <NuxtLink to="/service">Service Two</NuxtLink>
                    <NuxtLink to="/service">Service Three</NuxtLink>
                    <NuxtLink to="/service">Service Four</NuxtLink>
                </div>
            </li>
            <li class="link" @click="navbarActiveLinks.isPagesActive = !navbarActiveLinks.isPagesActive">
                <NuxtLink to="/pages">Pages<Icon name="material-symbols:keyboard-arrow-down"/></NuxtLink>
                <div :class="[{'pages-active': navbarActiveLinks.isPagesActive}, 'dropdownlinks']">
                    <NuxtLink to="/pages">Team One</NuxtLink>
                    <NuxtLink to="/pages">Team Two</NuxtLink>
                    <NuxtLink to="/pages">Testimonials</NuxtLink>
                    <NuxtLink to="/pages">Case Study One</NuxtLink>
                    <NuxtLink to="/pages">Case Study Two</NuxtLink>
                    <NuxtLink to="/pages">Case Study Slider</NuxtLink>
                    <NuxtLink to="/pages">Login</NuxtLink>
                    <NuxtLink to="/pages">Register</NuxtLink>
                </div>
            </li>
            <li class="link" @click="navbarActiveLinks.isBlogActive = !navbarActiveLinks.isBlogActive">
                <NuxtLink to="/blog">Blog<Icon name="material-symbols:keyboard-arrow-down"/></NuxtLink>
                <div :class="[{'blog-active': navbarActiveLinks.isBlogActive}, 'dropdownlinks']">
                    <NuxtLink to="/blog">Blog One</NuxtLink>
                    <NuxtLink to="/blog">Blog Two</NuxtLink>
                    <NuxtLink to="/blog">Blog Three</NuxtLink>
                    <NuxtLink to="/blog">Blog Details</NuxtLink>
                </div>
            </li>
            <li class="link">
                <NuxtLink to="/contact">Contact</NuxtLink>
            </li>
        </ul>
        <div class="header-btn">
                <a href="#">Get A Quote</a>
        </div>
  </section>
</template>

<style scoped>
.navbar {
    width: 100vw;
    height: auto;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    background-color: #0060ff;
    padding: 0 8% 0 8%;
    font-size: 15px;
    top: 0;
    z-index: 100000;
}
.sticky {
    position: sticky;
    animation: stickyAnim 0.3s ease-out;
    animation-fill-mode: forwards;
}
@keyframes stickyAnim {
    from {
        top: -80px;
    }
    to {
        top: 0;
    }
}
.mobileButtons {
    width: 16%;
    min-height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.logo {
    display: flex;
    justify-content: center;
    align-items: center;
    align-self: flex-start;
    min-height: 80px;
}
.hamburger-button {
    width: 90px;
    height: 30px;
    display: none;
    background-color: #000000;
    color: #fff;
    border: none;
    border-radius: 5px;
    font-family: 'Open Sans', sans-serif;
    font-weight: 900;  
    font-size: 16px;
}
.hamburger-icon {
    font-size: 20px;
}
.links {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    width: 60%;
    list-style-type: none;
    font-size: 16px;
    color: #fff;
    height: 100%;
}

@keyframes fadeOut {
    from {
        top: 120px;
        opacity: 0;
    }
    to {
        top: 80px;
        opacity: 1;
    }
}

.link {
    color: #fff;
    position: relative;
    display: flex;
    min-width: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
}
@media (min-width: 800px) {
    .link {
        height: 80px;
    }
    .link:hover .dropdownlinks {
    display: flex;
    justify-content: space-evenly;
    align-content: center;
    flex-direction: column;
    animation-name: fadeOut;
    animation-iteration-count: 1;
    animation-duration: 300ms;
    animation-fill-mode: forwards;
    left: 0;
}
}

.dropdownlinks {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    width: 250%;
    font-size: 13px;
    box-shadow: 0px 2px 5px 0px rgba(0,0,0,0.2);
    z-index: 1;
}
.dropdownlinks a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}
.dropdownlinks a:hover {
    color: #fff;
    background-color: #0060ff;
    transition: 300ms;
}
.header-btn {
    display: flex;
    justify-content: center;
    align-items: center;
    align-self: flex-start;
    background-color: rgb(8, 106, 216);
    width: 150px;
    height: 60px;
    border: none;
    border-radius: 5px;
    outline: none;
    cursor: pointer;
    margin: 10px 0;
}

a {
    cursor: pointer;
    text-decoration: none;
    color: #fff;
    display: flex;
    flex-wrap: nowrap;
}

@media (max-width: 800px) {
    .navbar {
        flex-direction: column;
        justify-content: space-between;
    }
    .mobileButtons {
        width: 100%;
        justify-content: space-between;
    }
    .logo {
        width: auto;
    }
    .links {
        display: none;
        flex-direction: column;
        width: 100%;
        align-items: flex-start;
        padding: 10px 20px;
        background-color: rgb(0, 123, 255);
        margin-bottom: 10px;
    }
    .hamburger-active {
        display: flex !important;
        animation: hamburgerActive 0.3s ease;
        height: auto;
        flex-wrap: nowrap;
    }
    @keyframes hamburgerActive {
        0% {
            height: 0;
            opacity: 0;
        }
        80% {
            height: 200px;
            opacity: 0;
        }
        100% {
            height: 200px;
            opacity: 1;
        }
    }
    .link {
        width: 100%;
        align-items: flex-start;
        min-height: 30px;
        flex-direction: column;
    }
    .link a {
        width: 100%;
        height: 30px;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        border-radius: 5px;
        padding-left: 10px;
    }
    .link a:hover {
        background-color: rgb(204, 204, 204);
        transition: 300ms;
    }
    .link .dropdownlinks {
        position: static;
        display: none;
        flex-direction: column;
        align-items: flex-start;
        width: 100%;
        background-color: transparent;
        box-shadow: none;
        padding: 5px 5px 5px 15px;
    }
    .link .dropdownlinks a {
        color: #fff;
        width: 100%;
        height: 30px;
        border-radius: 5px;
    }
    .home-active {
        display: flex !important;
        animation: homeActive 0.2s ease;
        height: auto;
        flex-wrap: nowrap;
    }
    @keyframes homeActive {
        from {opacity: 0; height: 0;}
        to {opacity: 1; height: 190px;}
    }
    .service-active {
        display: flex !important;
        animation: serviceActive 0.2s ease;
        height: auto;
        flex-wrap: nowrap;
    }
    @keyframes serviceActive {
        from {opacity: 0; height: 0;}
        to {opacity: 1; height: 130px;}
    }
    .pages-active {
        display: flex !important;
        animation: pagesActive 0.2s ease;
        height: auto;
        flex-wrap: nowrap;
    }
    @keyframes pagesActive {
        from {opacity: 0; height: 0;}
        to {opacity: 1; height: 250px;}
    }
    .blog-active {
        display: flex !important;
        animation: blogActive 0.2s ease;
        height: auto;
        flex-wrap: nowrap;
    }
    @keyframes blogActive {
        from {opacity: 0; height: 0;}
        to {opacity: 1; height: 130px;}
    }
    .header-btn {
        display: none;
    }
    .hamburger-button {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        
    }
}

</style>