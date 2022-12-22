<template>
  <main class="main" id="main">
    <TheBanner />
    <ThePresentation />
    <TheMedias />
  </main>
</template>


<script>
 import ThePresentation from "../components/ThePresentation.vue"
 import TheBanner from '../components/TheBanner.vue'
 import TheMedias from '../components/TheMedias.vue'

 export default {
  components:{
    ThePresentation, TheBanner, TheMedias
  },
  
 }
</script>


<style lang="scss">
@import '../assets/style.scss';

  .main{
    position: relative;
    z-index: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column nowrap;
    overflow: hidden;
  }
  
</style>