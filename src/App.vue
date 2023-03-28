<script>
  import TheHeader from './components/TheHeader.vue';
  import TheFooter from './components/TheFooter.vue';
  import ListSeries from './components/ListSeries.vue';

  export default {
    components:{
      TheHeader,
      TheFooter,
      ListSeries
    }
  }
</script>

<template>
  <TheHeader />

  <ListSeries />

  <TheFooter/>

</template>

<style lang="scss">
@use "./styles/_general.scss";


</style>
