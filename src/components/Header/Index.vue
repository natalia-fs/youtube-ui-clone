<template>
  <div class="header-container">
    <div class="home">
      <img class="menu-icon" src="../../assets/MenuIcon.svg" alt="Menu">
      <img class="logo" src="../../assets/youtube-logo.svg" alt="Youtube">
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
export default {
  name: 'Header',
  props: {
    msg: String
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
