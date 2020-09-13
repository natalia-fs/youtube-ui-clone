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
      <div class="story"></div>
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

  .home{
    display: flex;
    width: 240px;  
    align-items: center;
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
    .story{
      width: 32px;
      height: 32px;
      margin: .2rem;
      border-radius: 50%;
      background-color: var(--sidebar);
    }
  }
}
</style>
