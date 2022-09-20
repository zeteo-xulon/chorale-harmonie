<template>
  <header>
      <img class="logo" src="./icons/logo_harmonie.jpg" alt="logo harmonie" />
      <nav>
        <RouterLink class="nav__link" to="/">Accueil</RouterLink>
        <RouterLink class="nav__link" to="/contact">Contact</RouterLink>
      </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../assets/style.scss";

header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-flow: raw nowrap;
    width: 100%;
    background: $bgPrimary;
    padding: 1rem;
  }

  .logo{
    height: 100px;
    width: 100px;
    box-sizing: border-box;
    object-fit: cover;
    border-radius: 50%;
  }

  nav{
    display:flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
  }

  .nav__link{
    text-decoration: none;
    font-weight: bold;
    color: $secondary;
    font-size: 1.5rem;
    transition: .2s all;
    
  }
  a:hover{
      color: $tertiary;
    }
</style>