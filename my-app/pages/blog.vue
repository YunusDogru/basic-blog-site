<template>
        <Loading/>
        <div class="wrapper">
        <TopBar/>
        <NavBar/>
        <SubLinksFirst :header="'Blog One'" :links="['Home', 'Blog One']"/>
        <Blogs :blogCount="[1,2,3,4,5,6]"/>
        <ServiceSection2/>
        <Partners/>
        <Footer/>
       <BottomLink/>
        </div>
</template>
