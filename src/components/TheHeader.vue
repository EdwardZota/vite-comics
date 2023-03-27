<script>
export default {
    name:"TheHeader",
    data(){
        return{
            navList:[
                {
                    href:"#characters",
                    text:"characters",
                },
                {
                    href:"#comics",
                    text:"comics",
                },
                {
                    href:"#movies",
                    text:"movies",
                },
                {
                    href:"#tv",
                    text:"tv",
                },
                {
                    href:"#games",
                    text:"games",
                },
                {
                    href:"#collectibles",
                    text:"collectibles",
                },
                {
                    href:"#videos",
                    text:"videos",
                },
                {
                    href:"#fans",
                    text:"fans",
                },
                {
                    href:"#news",
                    text:"news",
                },
                {
                    href:"#shop",
                    text:"shop",
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
            <img src="/dc-logo.png" alt="DC Logo">
        </div>
        <nav>
            <ul>
                <li v-for="(link,index) in navList" :key="index">
                    <a :href="link.href">{{link.text.toUpperCase()}}</a>
                </li>
            </ul>
        </nav>
        </div>
        

    </header>

</template>

<style scoped lang="scss">
@use "../styles/partials/variables.scss";

header {
  background-color: variables.$color-navbar-bg;
  padding: 20px 0;
}

.container{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 1300px;
    margin: auto;
}

ul{
    display: flex;
    li{
    list-style: none;
    &:hover a{
        color: variables.$color-primary;
    }
    }
    a{
    color: black;
    text-decoration: none;
    padding: 0 12px;

}}



</style>
