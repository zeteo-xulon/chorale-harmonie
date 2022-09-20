<template>
  <article class="presentation">
    <img class="presentation__img" src="./icons/harmonie_logo_squared.png" alt="logo de la chorale" />

    <aside class="presentation__paragraph">
     <p class="presentation__txt">
        La Chorale Harmonie est une chorale Gospel à Paris depuis 2020. Notre choeur rassemble des chanteurs amateurs de confession chrétienne, avec une passion commune, chanter ! Notre répertoire alterne des chants gospel, des spirituals et des chants de liberté.</p>

      <p class="presentation__txt">
          Ce qui nous fait vibrer ? Les rythmes du Gospel, ses harmonies, et l’énergie que ça procure ! Nos représentations, toute l'année, sont toujours des moments forts où l’on peut transmettre notre passion au public. </p>

      <p class="presentation__txt">
          Venez nous invitez en représentation gospel dans votre établissement, contactez nous pour plus d'informations !</p>
    </aside>

  </article>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
@import '../assets/style.scss';

.presentation{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-flow: row nowrap;
  background: $bgSecondary;
  width: 100%;
  gap: 2rem;
  padding: 1rem;;
  &__img{
    width: 30%;
    min-width: 150px;
    background: $bgPrimary;
    border-radius: 50%;
  }
  &__paragraph{
    display: grid;
    gap: 2rem;
    grid-template: repeat(3, 1fr) / 1fr;
  }
  &__txt{
    color: $txtTertiary;
    font-size: 1.3rem;
    width: 90%;
  }
}

@media screen and (max-width: 640px) {
  .presentation{
    justify-content: space-between;
    flex-flow: column nowrap;
    &__img{
      width:70%;
    }
    &__txt{
      width:100%;
    }
  }
}
</style>>
