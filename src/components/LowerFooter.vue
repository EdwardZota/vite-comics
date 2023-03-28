<script>
export default {
    name: "LowerFooter",
    data() {
        return {
            listSocial: [
                {
                    href: "#facebook",
                    img: "/footer-facebook.png",
                    name: "facebook"
                },
                {
                    href: "#twitter",
                    img: "/footer-twitter.png",
                    name: "twitter"
                },
                {
                    href: "#youtube",
                    img: "/footer-youtube.png",
                    name: "youtube"
                },
                {
                    href: "#periscope",
                    img: "/footer-periscope.png",
                    name: "periscope"
                },
                {
                    href: "#pinterest",
                    img: "/footer-pinterest.png",
                    name: "pinterest"
                }
            ]
        }
    }
}
</script>


<template>
    <div class="container">
        <div class="box">
            <button>SING-UP NOW</button>
            <nav>
                <ul>
                    <h3>FOLLOW US</h3>
                    <li v-for="(social, i) in listSocial" :key="i">
                        <a :href="social.href"><img :src="social.img" :alt="social.name"></a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

.container {
    background-color: #303030;
    width: 100%;
}

.box {
    @include mixins.width-m-auto;
    @include mixins.d-flex-space-between;
    padding: 30px 0;

    ul {
        display: flex;
        align-items: center;

        h3 {
            color: variables.$color-primary;
            transition: all 1s;

            &:hover {
                font-weight: bolder;
                color: white;
            }
        }

        li {
            padding: 15px;
            transition: all 1s;

            &:hover {
                transform: scale(1.5);
            }
        }
    }
}

button {
    padding: 10px;
    background: none;
    border: 1px solid variables.$color-primary;
    color: white;
    transition: all 1s;

    &:hover {
        color: black;
        background-color: white;
        transform: scale(1.5);
        font-weight: bolder;
    }
}
</style>
    
