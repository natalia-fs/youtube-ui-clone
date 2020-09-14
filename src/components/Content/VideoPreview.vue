<template>
  <div class="preview-container">
    <div class="thumb">
      <img :src="formatThumbnail" alt="Preview" />
    </div>
    <div class="info">
      <div class="channel-thumb">
        <img :src="formatThumbnail" alt="Channel" />
      </div>
      <div class="metadata">
        <strong class="video-title">{{videoName}}</strong>
        <strong class="channel-name">{{channelName}}</strong>
        <strong class="video-info">{{views}} visualizações • há {{upload}}</strong>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props:{
        videoName: String,
        channelName: String,
        views: Number,
        upload: String,
        videoThumb: String,
    },
    computed: {
        formatThumbnail(){
        return require(`../../assets/img/${this.videoThumb}`);
    }
  }
};
</script>

<style scoped lang="scss">
.preview-container {
  display: flex;
  flex-direction: column;
  max-width: 253px;
  max-height: 252px;
  align-items: center;
  margin: 0 .6rem 1rem .6rem;

  .thumb {
    margin-left: .2rem;
    img {
      width: 253px;
      height: 142px;
      object-fit: cover;
    }
  }
  .info {
    display: flex;
    flex-direction: row;
    color: var(--gray);
    font-size: 14px;
    width: 253px;
    max-height: 112px;
    padding-left: .2rem;
    padding-top: .8rem;
    .channel-thumb {
      margin-right: .8rem;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 36px;
      height: 36px;
      img {
        border-radius: 50%;
        background-color: blueviolet;
        width: 38px;
        height: 38px;
        object-fit: none;
      }
    }
    .metadata{
        display: flex;
        flex-direction: column;
        .video-title{
            max-height: 40px;
            color: var(--white);
            padding-bottom: .2rem;
        }
        .channel-name{
            padding-bottom: .2rem;
            font-weight: 400;
        }
        .video-info{
            font-weight: 400;
        }
    }
  }
}
</style>