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
    display: flex;
    flex-direction: column;
    background-color: var(--sidebar);
    max-height: calc(100vh - 56px);
    grid-area: SIDEBAR;
    grid-template-rows: 147px 267px auto;
    grid-template-areas:
      "NAV"
      "USER"
      "SUBS"
    ;
}
</style>