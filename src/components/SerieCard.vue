<script>
export default {
    name: "SerieCard",
    props: {
        image: String,
        title: String
    }
}

</script>

<template>
    <div class="series-card">
        <img :src="image" :alt="title">
        <h3>{{ title.toUpperCase() }}</h3>

    </div>
</template>

<style lang="scss" scoped>
.series-card {
    width: 200px;
    height: 400px;
    padding-bottom: 50px;
    position: relative;

    img {
        width: 100%;
        height: 300px;
        transition: all 1s;
    }

    h3 {
        padding-top: 10px;
        font-weight: 500;
    }

    &:hover img {
        transform: scale(1.3);
        box-shadow: -5px -5px 30px 5px red, 5px 5px 30px 5px blue;
        opacity: 0.5;
    }

    &:hover h3 {
        position: absolute;
        top: 40%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 30px;
        font-weight: bolder;
    }

}
</style>