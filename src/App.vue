<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/youtube-logo.svg"> -->
    <Header/>
    <Sidebar/>
  </div>
</template>
<script>
import './styles/global.scss'
import Header from './components/Header/Index';
import Sidebar from './components/Sidebar/Index';
export default {
  components: {
    Header,
    Sidebar
  }
}
</script>
<style>
#app{
  display: grid;
  height: 100vh;
  grid-template-columns: 240px auto;
  grid-template-rows: 56px auto;
  grid-template-areas:
  "HEADER HEADER"
  "SIDEBAR MAIN"
}
</style>
