<script>
import SerieCard from './SerieCard.vue';

export default {
    name: "ListSeries",
    components: {
        SerieCard
    },
    data() {
        return {
            listSeries: [
                {
                    "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                    "price": "$3.99",
                    "series": "Batman / Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                    "price": "$4.99",
                    "series": "Batman / Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}

</script>

<template>
    <div id="jumbotron">
    </div>
    <main>
        <span>CURRENT SERIES</span>
        <div id="Series">
            <div v-for="(serie, i) in listSeries" :key="i">
                <SerieCard :image="serie.thumb" :title="serie.series" />
            </div>

        </div>
        <div id="btn">
            <button>LOAD MORE</button>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins';
@use '../styles/partials/variables';

#jumbotron {
    background-image: url(/jumbotron.jpg);
    height: 500px;
    background-size: cover;
    margin-bottom: 50px;
}

span {
    display: inline-block;
    padding: 10px 20px;
    position: absolute;
    top: -68px;
    left: 0;
    background-color: variables.$color-primary;
    font-weight: bolder;

}

#Series {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    height: 800px;
}

#btn {
    display: flex;
}

button {
    background-color: variables.$color-primary;
    color: variables.$color-navbar-bg;
    padding: 10px 30px;
    margin: 30px auto;
    font-weight: bolder;
    border: none;

}
</style>