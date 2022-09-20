<template>
  <footer class="footer">
    <p class="footer__text">Conception : <a class="footer__text--link" href="mailto:n.dreux@live.fr" >Nicolas DREUX </a>	| ©2022 - Chorale Harmonie</p>
  </footer>
</template>


<script> export default {} </script>


<style lang="scss" scoped>
@import '../assets/style.scss';

.footer{
  height:100px;
  width:100%;
  display: flex;
  justify-content: center;
  align-items: center;
  &__text{
    font-size: 1rem;
    font-weight: 700;
    text-align: center;
    &--link{
      text-decoration: none;
      color: $linkPrimary;
      &:hover{
        color: $linkSecondary;
      }
    }
  }
}

</style>