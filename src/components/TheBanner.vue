<template>
  <section class="banner">
    <video class="banner__video" 
    id="bannerVideo"  
    src="./medias/harmonie_video_light.mp4"
    autoplay 
    loop 
    muted 
    playsinline >
    Votre navigateur ne permet pas la lecture de la vidéo.
    </video>
    <div class="banner__fader">
      <h1 class="banner__title">Chorale Harmonie</h1>
      <h2 class="banner__sub">Bienvenue sur le site de la chorale Harmonie</h2>
    </div>
  </section>
</template>


<script>
export default {}
</script>


<style lang="scss" scoped>
  @import '../assets/style.scss';

  .banner{
    position: relative;
    width: 100%;
    height: 600px;
    &__video{
      z-index: 1;
      object-fit: cover;
      -o-object-fit: cover;
      object-position: center;
      width: 100%;
      height: 100%;
    }
    &__fader{
      display: flex;
      flex-flow: column nowrap;
      position: absolute;
      z-index: 2;
      background-color: rgba(0, 0, 0, .7);
      width: 100%;
      bottom: 0rem;
      padding: .5rem 1rem;
    }
    &__title{
      z-index: 3;
      font-size: 3rem;
      color: $txtSecondary;
      font-weight: 900;
    }
    &__sub{
      z-index: 3;
      font-size: 1.5rem;
      font-weight: 400;
      color: $txtSecondary;
    }
  }

  @media screen and (max-width:$sm) {
    .banner{
      &__title{ font-size: clamp(16px, 10vw, 2rem); }
      &__sub{ font-size: clamp(16px, 10vw, 1.5rem); }
    }
  }
</style>>
