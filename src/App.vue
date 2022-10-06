<script>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'

export default {
  components: {
    TheHeader, TheFooter
  }
}
</script>

<template>
  <div class="container">
    <TheHeader />
    <RouterView />
    <TheFooter />
  </div>
</template>


<style lang="scss">
@import './assets/style.scss';
  
*{
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
  @include textFont;
}
.container{
  display: flex;
    flex-flow: column nowrap;
    justify-content: space-between;
    align-items: center;
    min-height: 100vh;
}

</style>