<template>
  <section class="contact-square">
    <h1 class="contact-square__title">Contactez nous</h1>
    <p class="contact-square__text">Si vous souhaitez plus de renseignements, vous pouvez nous contacter en appuyant sur le bouton juste en dessous.</p>
    <div class="contact-square__btn-container">
      <a class="contact__btn" href="mailto:renice.aka@gmail.com">Contacter</a>
    </div>
    
  </section>
</template>


<script>
export default {}
</script>


<style lang="scss" scoped>
@import '../assets/style.scss';

.contact-square{
  display: flex;
  justify-content: center;
  align-content: space-between;
  flex-flow: column nowrap;
  width: 100%;
  height: 60%;
  gap: 1rem;
  padding: 1rem;
  border: 3px solid $secondary;
  border-radius: 10px;
  transition: all .25s;
  &__title{
    font-size: 1.5rem;
  }
  &__text{
    font-size: 1.1rem;
    text-align: justify;
  }
  &__btn-container{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }
  &:hover{
    border: 3px solid $tertiary;
  }
}

.contact__btn{
  width:10rem;
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