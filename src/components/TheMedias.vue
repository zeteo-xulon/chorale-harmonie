<template>
  <section class="media">
    <img class="media__image img01" src="./medias/01.jpg" alt="Image des choristes" />
    <img class="media__image img02" src="./medias/02.jpg" alt="Image des choristes" />
    <img class="media__image img03" src="./medias/03.jpg" alt="Image des choristes" />
    <img class="media__image img04" src="./medias/04.jpg" alt="Image des choristes" />
    <img class="media__image img05" src="./medias/05.jpg" alt="Image des choristes" />
    <img class="media__image img06" src="./medias/06.jpg" alt="Image des choristes" />
    
    <RouterLink class="more" to="/gallery"><span>+</span></RouterLink>
  </section>
</template>


<script> export default {
  data(){
    return{
      modal: false,
      img01: false,
      img02: false,
      img03: false,
      img04: false,
      img05: false,
      img06: false
    }
  },
} </script>


<style lang="scss" scoped>
@import '../assets/style.scss';

.media{
  position: relative;
  width: 100%;
  height: 100%;
  display: grid;
  grid: repeat(4, 250px) / repeat(4, 1fr);
  gap: .3rem;
  padding: .3rem;
  &__image{
    object-fit: cover;
    width: 100%;
    height: 100%;
    transition: all .25s;
    &:hover{
      transform: scale(1.025, 1.025);
      box-shadow: 2px 1px 3px 3px rgba(1,1,1,.3);
      border-radius: 10px;
    }
    &:active{
    transform: scale(1.05, 1.05);
    box-shadow: 2px 1px 3px 3px rgba(1,1,1,.3);
    border-radius: 10px;
    }
  }
}
.more{
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 3;
  font-size:10rem;
  color: rgba(255,255,255,.7);
  cursor: pointer;
  text-decoration: none;
  transition: all .25s;
  &:hover{
    transform: scale(1.05, 1.05);
  }
}

.img01{ grid-area: 1/1/3/5; }
.img02{ grid-area: 3/1/5/2; }
.img03{ grid-area: 3/3/4/5; }
.img04{ grid-area: 3/2/5/3; }
.img05{ grid-area: 4/3/5/4; }
.img06{ 
  grid-area: 4/4/4/4;
  filter: blur(.25rem);
  &:hover{ filter: blur(0rem); } 
  }
  .more{ grid-area: 4/4/4/4;}

@media screen and (max-width: $sm) {
  .media{
    grid-template: repeat(4, 250px) / repeat(2, 1fr);
    .img01{ grid-area: 1/1/2/3; }
    .img02{ grid-area: 2/1/4/2; }
    .img03{ grid-area: 2/2/3/2; }
    .img04{ grid-area: 3/2/4/2; }
    .img05{ grid-area: 4/1/4/2; }
    .img06{ grid-area: 4/2/4/3; }
    .more{ grid-area: 4/2/4/3;}
  }
}
@media screen and (min-width: $sm) and (max-width: $md) {
  .media{
    grid-template: repeat(4, 250px) / repeat(3, 1fr);
    .img01{ grid-area: 1/1/2/4; }
    .img02{ grid-area: 3/1/5/2; }
    .img03{ grid-area: 2/1/3/4; }
    .img04{ grid-area: 3/2/5/3; }
    .img05{ grid-area: 3/3/4/4; }
    .img06{ grid-area: 4/3/4/4; }
    .more{ grid-area: 4/3/4/4; }
  }
}

</style>

