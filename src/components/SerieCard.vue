<script>
export default {
    name:"SerieCard",
    props:{
        image:String,
        title:String
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
.series-card{
    width: 200px;
    padding-bottom: 50px;
    img{
        width: 100%;
        height: 300px;
    }
    h3{
        padding-top: 10px;
        font-weight: 500;
    }
}

</style>