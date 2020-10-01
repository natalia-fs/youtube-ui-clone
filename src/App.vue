<template>
  <div id="app">
    <Header/>
    <Sidebar/>
    <Content/>
  </div>
</template>
<script>
import './styles/global.scss'
import Header from './components/Header/Index';
import Sidebar from './components/Sidebar/Index';
import Content from './components/Content/Index';
export default {
  components: {
    Header,
    Sidebar,
    Content
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
@media(max-width: 1125px){
  #app{
    grid-template-columns: 74px auto;
    grid-template-rows: 56px auto;
  }
}
</style>
