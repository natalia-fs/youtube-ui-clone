<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/youtube-logo.svg"> -->
    <Header/>
  </div>
</template>
<script>
import './styles/global.scss'
import Header from './components/Header/Index';
export default {
  components: {
    Header,
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
