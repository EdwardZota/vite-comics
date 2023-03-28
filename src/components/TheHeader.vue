<script>
export default {
    name: "TheHeader",
    data() {
        return {
            navList: [
                {
                    href: "#characters",
                    text: "characters",
                },
                {
                    href: "#comics",
                    text: "comics",
                },
                {
                    href: "#movies",
                    text: "movies",
                },
                {
                    href: "#tv",
                    text: "tv",
                },
                {
                    href: "#games",
                    text: "games",
                },
                {
                    href: "#collectibles",
                    text: "collectibles",
                },
                {
                    href: "#videos",
                    text: "videos",
                },
                {
                    href: "#fans",
                    text: "fans",
                },
                {
                    href: "#news",
                    text: "news",
                },
                {
                    href: "#shop",
                    text: "shop",
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
                    <li v-for="(link, index) in navList" :key="index" :class="index == 1 ? 'selected' : ''">
                        <a :href="link.href">{{ link.text.toUpperCase() }}</a>
                    </li>
                </ul>
            </nav>
        </div>


    </header>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables.scss";
@use "../styles/partials/mixins";

header {
    background-color: variables.$color-navbar-bg;
}

.container {
    @include mixins.d-flex-space-between;
    @include mixins.width-m-auto;

    nav {
        line-height: 130px;

        ul {
            display: flex;

            a {
                color: black;
                text-decoration: none;
                padding: 0 12px;

            }
        }
    }
}



.selected {
    background-color: variables.$color-primary;
    transform: skew(-15deg);
}
</style>
