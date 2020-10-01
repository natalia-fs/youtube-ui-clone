<template>
  <div class="nav-container">
    <div class="item active">
      <div class="icon">
        <HomeIcon :size="22"/>
      </div>
      <p>Início</p>
    </div>
    <div class="item">
      <div class="icon">
        <TrendingIcon :size="22"/>
      </div>
      <p>Em alta</p>
    </div>
    <div class="item">
      <div class="icon">
        <SubsIcon :size="22"/>
      </div>
      <p>Inscrições</p>
    </div>
    <div class="item library">
      <div class="icon">
        <LibraryIcon :size="22"/>
      </div>
      <p>Biblioteca</p>
    </div>
  </div>
</template>

<script>
import HomeIcon from "vue-material-design-icons/Home";
import TrendingIcon from "vue-material-design-icons/Fire";
import SubsIcon from "vue-material-design-icons/YoutubeSubscription";
import LibraryIcon from "vue-material-design-icons/PlayBoxMultiple";
export default {
  components: {
    HomeIcon,
    TrendingIcon,
    SubsIcon,
    LibraryIcon
  }
}
</script>

<style lang="scss" scoped>
.nav-container{
  grid-area: NAV;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: .2rem 0;
  cursor: pointer;
  border-bottom: solid 1px var(--hover);
  .item{
    display: grid;
    grid-template-columns: 48px auto;
    flex-direction: row;
    align-items: center;
    font-weight: 400;
    font-size: 14px;
    width: 240px;
    height: 40px;
    padding: 0 1.4rem;
    &:hover{
      background-color: var(--hover);
    }
    color: var(--icon-secondary);
    &.active{
      color: var(--white);
      background-color: var(--hover);
      font-weight: 600;
    }
  }
  .item.library{
    display: none;
  }
}
@media(max-width: 1125px){
  .nav-container{
    border: none;
    align-items: flex-start;
    justify-content: flex-start;
    .item.library{
      display: flex;
    }
    .item{
      display: flex;
      flex-direction: column;
      width: 74px;
      height: 72px;
      padding: .6rem 0;
      p{
        font-size: .5rem
      }
      &:hover{
        background-color: inherit;
      }
      &.active{
        color: var(--white);
        background-color: inherit;
        font-weight: 600;
      }
    }
  }
}
</style>