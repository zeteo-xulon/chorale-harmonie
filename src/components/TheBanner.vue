<template>
  <section class="banner">

    <video v-show="sourceMedia === 1" id="bannerVideo" class="banner__video" autoplay loop muted playsinline>
      <source v-show="isMobileDevice" class="banner__video" src="./medias/harmonie_video_light.mp4" type="video/webm" >
      <source v-show="!isMobileDevice" class="banner__video" src="./medias/chorale-harmonie_Desktop_Version+.mp4" type="video/webm" >
    
      Votre navigateur ne permet pas la lecture de la vidéo.
    </video>
    <picture v-show="sourceMedia === 2" class="banner__picture">
      <img class="banner__picture" src="./medias/12_light.jpg" type="jpg" alt="image des chanteuses et chanteurs de la chorale">
    </picture>

    <div class="banner__fader">
      <h1 class="banner__title">Chorale Harmonie</h1>
      <h2 class="banner__sub">Bienvenue sur le site de la chorale Harmonie</h2>
    </div>

  </section>
</template>


<script>
export default {
  data(){
    return{
      sourceMedia: 1,
      isMobileDevice: false
    }
  },
  methods: {
    autoSwitch(){
      setInterval(()=> this.sourceMedia === 1 ? this.sourceMedia = 2 : this.sourceMedia = 1, 30000)
    },
    isMobile(){
     return window.innerWidth < 770 ? true : false ;
    }
  },
  beforeMount(){
    this.isMobileDevice = this.isMobile();
  },
  mounted(){
    this.autoSwitch()
  }
}
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
    &__picture{
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
      font-size: clamp(1.5rem, 14vw, 6rem);
      color: $txtSecondary;
      font-weight: 300;
      font-family: Symphonie, sans-serif;
    }
    &__sub{
      z-index: 3;
      font-size: clamp(16px, 6vw, 1.5rem);
      font-weight: 400;
      color: $txtSecondary;
    }
  }

  // @media screen and (max-width:$sm) {
  //   .banner{
  //     &__title{ font-size: clamp(16px, 10vw, 2rem); }
  //     &__sub{ font-size: clamp(16px, 10vw, 1.5rem); }
  //   }
  // }
</style>>
