<template>
  <footer class="footer" id="footer">
    <p class="footer__text">Conception : <a class="footer__text--link" href="mailto:n.dreux@live.fr" >Nicolas DREUX </a>	| ©2022 - Chorale Harmonie</p>
    <div class="popup-keys" id="popupContainer"></div>
  </footer>
</template>


<script> 
  export default {
    methods: {
      musicKeyParticle(){
        const keyColor = ["#4b8889", "#deb3a3", "#f4e1db", "#d5a634", "#c7cb98", "#f0e0c7", "#99a18a", "#f8b2bc", "#a0d0d1", "#d8a45b"];
        const keyNote = ["e", "g", "h", "m", "n", "s", "t", "w", "y", "g"];
        const randomColor = Math.floor(Math.random() * 10)
        const popupContainer = document.getElementById('popupContainer');
        const key = document.createElement('span');
        const size = Math.random().toFixed(2) * 2 +1;
        const plusMinus = Math.random() > 0.5 ? 1 : -1;

        key.innerText = keyNote[randomColor];
        popupContainer.appendChild(key);

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