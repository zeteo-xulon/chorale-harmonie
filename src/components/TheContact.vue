<template>
  <section class="contact">
    <h1 class="">Contactez nous</h1>
    <a class="contact__btn" href="mailto:n.dreux@live.fr">Contacter</a>
  </section>
</template>


<script>
export default {}
</script>


<style lang="scss" scoped>
@import '../assets/style.scss';

.form{
  width: 100%;
  height: 60%;
  border: 3px solid $secondary;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-content: space-between;
  flex-flow: column nowrap;
  gap: 1rem;
  padding: 1rem;
  &__title{ text-align: start; }
  &__btn-container{
    display:flex;
    justify-content: flex-end;
    align-items: center;
    gap: 5vw;
  }
}

button{
  padding: .5rem;
  font-weight: 700;
  border: 3px solid $secondary;
  border-radius: 5px;
  background-color: $secondary;
  color: $txtSecondary;
  text-decoration: none;
  cursor: pointer;
  &:hover{
    background-color: $bgPrimary;
    color: $secondary;
    transform: scale(.98,.98);
  }
}

</style>