<template>
  <div class="content-container">
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="256"
      upload="1 semana"
      videoThumb="thumb-vue.jpg"
      duration="19:45"
    />
    <VideoPreview
      videoName="CSS grid e suas vantagens"
      channelName="CSS ninja #2345"
      :views="2048"
      upload="2 semanas"
      videoThumb="thumb-css.jpg"
      duration="20:14"
    />
    <VideoPreview
      videoName="Semantic HTML"
      channelName="HTML5 School"
      :views="1024"
      upload="2 semanas"
      videoThumb="thumb-html.jpg"
      duration="8:00"
    />
    <VideoPreview
      videoName="Aprenda agora a programar com Angular"
      channelName="Devs Angular"
      :views="8112"
      upload="1 dia"
      videoThumb="thumb-angular.jpg"
      duration="36:27"
    />
    <VideoPreview
      videoName="Tutorial React 2020 [PT-BR]"
      channelName="React DEVELOPER BR 2"
      :views="972"
      upload="1 mês"
      videoThumb="thumb-react.jpg"
      duration="48:49"
    />
    <VideoPreview
      videoName="Javascript 'Baunilha'"
      channelName="JS em pt-BR"
      :views="4545"
      upload="1 semana"
      videoThumb="thumb-javascript.jpg"
      duration="25:13"
    />
    <VideoPreview
      videoName="Build better apps with Flutter"
      channelName="Another youtuber"
      :views="155"
      upload="1 semana"
      videoThumb="thumb-flutter.jpg"
      duration="29:10"
    />
    <VideoPreview
      videoName="Git para iniciantes - tudo o que você precisa saber!"
      channelName="Fullstack elástico"
      :views="9983"
      upload="1 ano"
      videoThumb="thumb-git.jpg"
      duration="24:56"
    />
    <VideoPreview
      videoName="CRUD em Laravel - Completo"
      channelName="Frontend laravel"
      :views="650"
      upload="3 semanas"
      videoThumb="thumb-laravel.jpg"
      duration="1:42:40"
    />
    <VideoPreview
      videoName="Primeiros passos com Node"
      channelName="Backend"
      :views="3603"
      upload="4 dias"
      videoThumb="thumb-node.jpg"
      duration="16:52"
    />
    <!--  -->
    <VideoPreview
      videoName="Vue.JS avançado"
      channelName="Vue for noobs"
      :views="5275"
      upload="2 semanas"
      videoThumb="thumb-vue.jpg"
      duration="55:06"
    />
        <VideoPreview
      videoName="Animações com CSS"
      channelName="CSS ninja #2345"
      :views="4096"
      upload="3 semanas"
      videoThumb="thumb-css.jpg"
      duration="14:09"
    />
    <VideoPreview
      videoName="HTML - Tag <section>"
      channelName="HTML5 School"
      :views="1824"
      upload="3 semanas"
      videoThumb="thumb-html.jpg"
      duration="9:00"
    />
    <VideoPreview
      videoName="Vantagens do Angular"
      channelName="Devs Angular"
      :views="8506"
      upload="1 semana"
      videoThumb="thumb-angular.jpg"
      duration="4:58"
    />
    <VideoPreview
      videoName="Tutorial React 2019 [PT-BR]"
      channelName="React DEVELOPER BR 2"
      :views="2478"
      upload="1 ano"
      videoThumb="thumb-react.jpg"
      duration="1:17:34"
    />
    <VideoPreview
      videoName="Como criar seu framework Javascript"
      channelName="JS em pt-BR"
      :views="6246"
      upload="5 meses"
      videoThumb="thumb-javascript.jpg"
      duration="1:02:18"
    />
    <VideoPreview
      videoName="Build better apps with Flutter [Part 2]"
      channelName="Another youtuber"
      :views="155"
      upload="1 semana"
      videoThumb="thumb-flutter.jpg"
      duration="28:41"
    />
    <VideoPreview
      videoName="Git para iniciantes - Como clonar um repositório"
      channelName="Fullstack elástico"
      :views="5983"
      upload="1 ano"
      videoThumb="thumb-git.jpg"
      duration="6:33"
    />
    <VideoPreview
      videoName="Migrations em Laravel"
      channelName="Frontend laravel"
      :views="1352"
      upload="3 meses"
      videoThumb="thumb-laravel.jpg"
      duration="19:45"
    />
    <VideoPreview
      videoName="Curso de Node.js - Aula 1"
      channelName="Backend"
      :views="5609"
      upload="4 meses"
      videoThumb="thumb-node.jpg"
      duration="30:04"
    />
  </div>
</template>

<script>
import VideoPreview from "./VideoPreview";
export default {
  components: {
    VideoPreview,
  },
  
};
</script>

<style scoped lang="scss">
.content-container {
  // display: grid;
  // // flex-wrap: wrap;
  // // grid-template-columns: 1fr 1fr 1fr 1fr;
  // grid-template-columns: repeat(auto-fill, minmax(25%, 1fr));
  // padding: 1rem .6rem;
  grid-area: MAIN;
  display: flex;
  background-color: var(--main);
  flex-direction: column;
  padding: 1rem;
  overflow-y: scroll;
}
@media(min-width: 513px){
  .content-container{
    display: grid;
    grid-template-columns: 50% 50%;
    justify-content: center;
    padding: 1rem .6rem;
  }
}
@media(min-width: 890px){
  .content-container{
    display: grid;
    grid-template-columns: 30% 30% 30%;
    justify-content: center;
  }
}
@media(min-width: 1145px){
  .content-container{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(25%, 1fr));
    padding: 1rem .6rem;
  }
}
</style>