<script>

import LowerFooter from './LowerFooter.vue';
import TopFooter from './TopFooter.vue';

export default {
    name:"TheFooter",
    components:{
      LowerFooter,
      TopFooter
    },
    data(){
        return{
            listFooter:[
                {
                    title:"dc comics",
                    links:["Characters","Comics","Movies","TV","Games","Videos","News"]
                },
                {
                    title:"shop",
                    links:["Shop DC","Shop DC Collectibles"]
                },
                {
                    title:"dc",
                    links:["Terms Of Use","Privacy policy(New)","Ad Choices","Advertising","Jobs","Subscriptions","Talent Workshops","CPSC Certificats","Ratings","Shop Help","Contact Us"]
                },
                {
                    title:"sites",
                    links:["DC","MAD Magazine","DC Kids","DC Universe","DC Power Visa"]
                }
            ]
        }
    }
}
</script>

<template>

    <TopFooter/>
    <footer>
        <nav>
            <ul v-for="(section,index) in listFooter" :key="index">
                <li >
                    <h3>{{ section.title.toUpperCase() }}</h3>
                    <ul>
                        <li v-for="(link,index) in section.links" :key="index">
                            <a href="#">{{link}}</a>
                        </li>
                    </ul>
                </li>
            </ul>
        </nav>
        <img src="/dc-logo-bg.png" alt="Logo DC">
    </footer>

    <LowerFooter/>

</template>

<style scoped>
    footer{
        background-image: url('/footer-bg.jpg');
        background-size: cover;
        width: 100%;
        height: 500px;
        position: relative;
        overflow: hidden;
    }

    nav{
        width: 1300px;
        margin: auto;
        padding: 35px 0;
        position: relative;
    }
    ul{
        list-style: none;
    }
    ul:nth-child(1n+3){
        position: absolute;
        top: 36px;
        left: 190px;
    }
    
    ul:nth-last-child(1){
        top: 36px;
        left: 350px;
    }

    h3{
        color: white;
        padding: 8px 0;
    }

    a{
        color: gray;
        text-decoration: none;
        display: inline-block;
        padding: 5px 0;
    }

    img{
        position: absolute;
        top: -80px;
        right: 280px;
        height: 700px;
    }


</style>
