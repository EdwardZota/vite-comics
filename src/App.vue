<script>
  import TheHeader from './components/TheHeader.vue';
  import TheFooter from './components/TheFooter.vue';

  export default {
    components:{
      TheHeader,
      TheFooter
    }
  }
</script>

<template>
  <TheHeader />

  <main>
    <span>contents goes here!</span>
  </main>

  <TheFooter/>

</template>

<style lang="scss">
@use "./styles/_general.scss";


</style>
