<template>
  <div class="content-container">
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-vue.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-css.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-html.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-angular.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-react.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-javascript.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-flutter.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-git.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-laravel.jpg"
    />
    <VideoPreview
      videoName="Vue.JS tutorial"
      channelName="Vue for noobs"
      :views="265"
      upload="1 semana"
      videoThumb="thumb-node.jpg"
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
  display: flex;
  flex-wrap: wrap;
  grid-area: MAIN;
  background-color: var(--main);
  padding: 1rem .6rem;
  overflow-y: scroll;
}
</style>