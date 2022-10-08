<template>
  <main class="main" id="main">
    <TheBanner />
    <ThePresentation />
    <TheMedias />
  </main>
</template>


<script>
 import ThePresentation from "../components/ThePresentation.vue"
 import TheBanner from '../components/TheBanner.vue'
 import TheMedias from '../components/TheMedias.vue'

 export default {
  components:{
    ThePresentation, TheBanner, TheMedias
  },
  methods: {
    musicKeyParticle(){
      const keyColor = ["#4b8889", "#deb3a3", "#f4e1db", "#d5a634", "#c7cb98", "#f0e0c7", "#99a18a", "#f8b2bc", "#a0d0d1", "#d8a45b"];
      const keyNote = ["e", "g", "h", "m", "n", "s", "t", "w", "y", "g"];
      const randomColor = Math.floor(Math.random() * 10)
      const main = document.getElementById('main');
      const key = document.createElement('span');
      const size = Math.random().toFixed(2) * 2 +1;
      const plusMinus = Math.random() > 0.5 ? 1 : -1;

      key.innerText = keyNote[randomColor];
      main.appendChild(key);

      key.style.position = "absolute";
      key.style.zIndex = 100;
      key.style.opacity = 0;
      key.style.fontSize = size+"rem";
      key.style.fontFamily= "MusicKey"
      key.style.color = keyColor[randomColor];
      key.style.top = Math.random() * 100 + 50 + "%";
      key.style.left = Math.random() *100 + "%";
      key.style.setProperty('--left', Math.random() * 100 * plusMinus +'%');
      key.style.animation = "keyMovement 30s both";

      setTimeout(() => { key.remove() }, 15000);
    },
    generateMusicKeyParticle(){
      setInterval(()=>  this.musicKeyParticle(), 1000);
    }
  },
  mounted(){
    this.generateMusicKeyParticle();
  }
 }
</script>


<style lang="scss">
@import '../assets/style.scss';

  .main{
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column nowrap;
    overflow: hidden;
  }
  .music-key{
    font-family: MusicKey, sans-serif;
    position: absolute;
    border-radius: 50%;
    opacity: 0;
    animation: keyMovement 8s both;
    filter: hue-rotate(0deg);
  }

  @keyframes keyMovement {
    70%{
    top: -250px;
    left: var(--left);
    opacity: 1;
    filter: hue-rotate(720deg);
  }
  }
</style>