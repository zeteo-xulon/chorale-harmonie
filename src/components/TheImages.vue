<template>
<section class="uc">
  <h1 class="uc__txt">Cette page est en cours de construction</h1>
  <img src="./medias/builder-drilling.gif" alt="animation d'un ouvrier au travail" class="uc__img" />
  </section>
  
</template>

<script>
export default {
  data(){
    return {
      listOfImages: [
        {
          key: 1,
          source: "01.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 2,
          source: "02.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 3,
          source: "03.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 4,
          source: "04.jpg",
          alt: "Image de la chorale Harmonie"
        },
          {
          key: 5,
          source: "05.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 6,
          source: "06.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 7,
          source: "07.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 8,
          source: "08.jpg",
          alt: "Image de la chorale Harmonie"
        },
          {
          key: 9,
          source: "09.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 10,
          source: "10_light.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 11,
          source: "11.jpg",
          alt: "Image de la chorale Harmonie"
        },
         {
          key: 12,
          source: "12_light.jpg",
          alt: "Image de la chorale Harmonie"
        },
      ],
      listOfVideos: [
        { key: 1,
        source: "01_light.mp4",
        alt: "video de la chorale harmonie",
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style.scss';

.uc{
  @include centered;
  flex-flow: column nowrap;
  padding: 1rem;
  &__txt{
    font-size: clamp(1rem, 5vw, 2rem);;
    text-align: center;
    color: $secondary;
    transition: all .25s;
    &:hover{
      color: $tertiary;
    }
  }
  &__img{
    width:80%;
    min-width: 300px;
  }

}

</style>