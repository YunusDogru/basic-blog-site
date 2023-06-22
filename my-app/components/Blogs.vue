<template>
    <section class="blogs">
        <div class="blog-header">
            <span>Blogs</span>
            <h2>Blog & News</h2>
        </div>
        <div class="blog-content">
            <div class="blog-box" v-for="i in blogCount" :key="`box${i}`">
                <h2 class="post-title">
                    <a href="#">Build Your Website Into Design Automatically</a>
                </h2>
                <p>Rearrange the entire color palette,
                    making your site unique and beatiful.
                </p>
                <div class="post-footer">
                    <span>
                        <Icon class="post-icon" name="fluent:folder-open-vertical-16-regular"/>
                        <a href="#">Fusion</a>
                    </span>
                    <span>
                        <Icon class="post-icon" name="octicon:person-16"/>
                        <a href="#" title="Posts by admin" rel="author">by admin</a>
                    </span>
                </div>
            </div>
        </div>
    </section>
  
</template>

<script setup>

const props = defineProps({
    blogCount: {
        type: Array,
        default: [1,2,3]
    }
});

</script>
<style scoped>
.blogs {
    display: flex;
    padding: 40px 0 80px 0;
    align-items: center;
    flex-direction: column;
    width: 100%;
    background-color: rgb(244, 249, 252);
}
.blog-header {
    height: 250px;
    text-align: center;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.blog-header span {
    color: rgb(102, 102, 102);
    position: absolute;
    transform: translateY(-50px);
    font-size: 15px;
}
.blog-header h2 {
    font-size: 45px;
    font-weight: bold;
}
.blog-content {
    width: 80%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
.blog-box {
    width: 30%;
    background-color: #fff;
    margin: 0 15px 30px 15px;
    padding: 40px 25px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    text-align: center;
}
@media (max-width: 1200px) {
    .blog-box {
        width: 40%;
    }
}
@media (max-width: 800px) {
    .blog-box {
        width: 100%;
    }
}
.blog-box:hover {
    background-image: url("http://webangon.com/html/bisness/img/4.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    animation: bgUp 0.5s ease-out;
    animation-fill-mode: forwards;
}
.blog-box:hover * {
    color: #fff;
}
@keyframes bgUp {
    from {
        background-position: top;
    }
    to {
        background-position: center;
    }
}
.post-title {
    padding-bottom: 15px;
    font-size: 20px;
    font-weight: 600;
    line-height: 35px;
    text-transform: capitalize;
}
.post-title a {
    text-decoration: none;
    color: #000000;
    transition: color 0.3s ease-out;
}
.post-title a:hover {
    color: rgb(0, 96, 255);
}
.blog-box p {
    border-bottom: 1px solid rgb(221, 221, 221);
    color: rgb(122, 133, 149);
    font-size: 13px;
    font-weight: 500;
    line-height: 30px;
    padding-bottom: 25px;
    margin-bottom: 25px;
    text-align: center;
}
.post-footer {
    height: 20px;
    width: 90%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.post-footer span{
    color: rgb(122, 133, 149);
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.post-footer span .post-icon {
    font-size: 18px;
}
.post-footer span a {
    text-decoration: none;
    color: rgb(122, 133, 149);
    white-space: nowrap;
    margin-left: 4px;
    font-size: 15px;
}
</style>