<template>
  <div class="contact">
    <TheContact />
  </div>
</template>

<script>
import TheContact from '../components/TheContact.vue'

export default {
  components: { TheContact }
}
</script>

<style lang="scss" scoped>
@import '../assets/style.scss';

  .contact{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    text-align: center;
    color: $secondary;
    padding: 2rem calc(.5rem + 7vw);
  }
</style>
