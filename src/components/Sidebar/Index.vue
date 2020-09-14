<template>
 <div class="sidebar-container">
   <Navigation />
   <UserData />
   <Subs />
 </div>
</template>

<script>
import Navigation from './Navigation.vue'
import UserData from './UserData.vue'
import Subs from './Subs.vue'
export default {
  components: {
    Navigation,
    UserData,
    Subs,
  }
}
</script>

<style lang="scss" scoped>
.sidebar-container{
    display: grid;
    flex-direction: column;
    background-color: var(--sidebar);
    max-height: calc(100vh - 56px);
    grid-area: SIDEBAR;
    grid-template-rows: 128px 248px auto;
    grid-template-areas:
      "NAV"
      "USER"
      "SUBS"
    ;
    overflow-y: scroll;
    overflow-x: hidden;
    &::-webkit-scrollbar{
    width: 8px;
    }
    &::-webkit-scrollbar-thumb{
      background-color: var(--hover);
    }
}
</style>