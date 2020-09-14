<template>
  <div class="header-container">
    <div class="home">
      <img class="menu-icon" src="../../assets/MenuIcon.svg" alt="Menu">
      <img class="logo" src="../../assets/youtube-logo.svg" alt="Youtube">
    </div>
    <div class="search-bar">
      <input type="text" placeholder="Pesquisar" class="search">
      <button class="search"><SearchIcon :size="20"/></button>
    </div>
    <div class="stories">
      <div class="story"></div>
      <div class="story"></div>
      <div class="story"></div>
      <div class="story profile"></div>
    </div>
  </div>
</template>

<script>
import SearchIcon from "vue-material-design-icons/Magnify";
export default {
  name: 'Header',
  props: {
    msg: String
  },
  components: {
    SearchIcon,
  }
}
</script>

<style lang="scss" scoped>
.header-container{
  grid-area: HEADER;
  display: flex;
  flex-direction: row;
  background-color: var(--header);
  justify-content: space-between;
  align-items: center;
  box-shadow: rgba(0,0,0,.1) 0 1px 0 0;
  z-index: 2;

  .home{
    display: flex;
    width: 170px;  
    align-items: center;
    justify-content: space-around;
    padding: 0 1rem;
    .menu-icon{
      width: 18px;
      height: 16px;
      cursor: pointer;
    }
    .logo{
      width: 80px;
      height: 24px;
      margin-left: 1rem;
      cursor: pointer;
    }
  }
  .search-bar{
    height: 30px;
    display: flex;
    flex-direction: row;
    align-items: center;
    input.search, button.search{
      max-height: 30px;
      height: 30px;
    }
    input{
      max-width: 575px;
      width: 575px;
      background-color: var(--searchbar);
      border-top-left-radius: 4px;
      border-bottom-left-radius: 4px;
      border: 1px solid var(--hover);
      padding: .4rem;
      color: var(--gray);
      font-size: 16px;
    }
    button{
      width: 65px;
      background-color: var(--button);
      border-top-right-radius: 4px;
      border-bottom-right-radius: 4px;
      cursor: pointer;
      color: var(--search-icon);
    }
  }
  .stories{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    margin: 0 .8rem;
    .story{
      width: 32px;
      height: 32px;
      margin: .2rem;
      border-radius: 50%;
      background-color: var(--sidebar);
    }
    .story.profile{
      background-color: var(--hover);
    }
  }
}
</style>
