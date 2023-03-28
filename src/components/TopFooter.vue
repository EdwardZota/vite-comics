<script>
export default {
    name: "TopFooter",
    data() {
        return {
            listMarket: [
                {
                    href: "#digital-comics",
                    img: "/buy-comics-digital-comics.png",
                    name: "digital-comics"
                },
                {
                    href: "#dc-merchandise",
                    img: "/buy-comics-merchandise.png",
                    name: "dc-merchandise"
                },
                {
                    href: "#subscription",
                    img: "/buy-comics-subscriptions.png",
                    name: "subscription"
                },
                {
                    href: "#comic-shop-locator",
                    img: "/buy-comics-shop-locator.png",
                    name: "comic-shop-locator"
                },
                {
                    href: "#dc-power-visa",
                    img: "/buy-dc-power-visa.svg",
                    name: "dc-power-visa"
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="box">
            <ul>
                <li v-for="(product, i) in listMarket" :key="i" class="item">
                    <a :href="product.href"><img :src="product.img" :alt="product.name"><span>{{ product.name.toUpperCase()
                    }}</span></a>
                </li>
            </ul>

        </div>

    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

.container {
    background-color: variables.$color-primary;
    height: 200px;
    width: 100%;

}

.item a,
.item img {
    transition: all 1s;
}

.item:hover a {
    color: black;
}

.item:hover img {
    filter: invert(100%);
    transform: scale(1.3)
}

.box {
    @include mixins.width-m-auto;
    height: 100%;

    ul {
        @include mixins.d-flex-space-between;
        height: 100%;

        a {
            text-decoration: none;
            color: white;

            img {
                vertical-align: middle;
                height: 60px;
                padding-right: 15px;
            }
        }
    }
}
</style>