<script>
 import ThePresentation from "../components/ThePresentation.vue"
 import TheBanner from '../components/TheBanner.vue'
 import TheMedias from '../components/TheMedias.vue'

 export default {
  components:{
    ThePresentation, TheBanner, TheMedias
  }
 }
</script>

<template>
  <main class="main">
    <TheBanner />
    <ThePresentation />
    <TheMedias />
  </main>
</template>

<style lang="scss" scoped>
@import '../assets/style.scss';

  .main{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column nowrap
  }
</style>