<template>
  <div class="preview-container">
    <div class="thumb">
      <img :src="formatThumbnail" alt="Preview" />
      <div class="duration">{{duration}}</div>
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
      <div class="options">
        <DotsIcon />
      </div>
    </div>
  </div>
</template>

<script>
import DotsIcon from "vue-material-design-icons/DotsVertical";
export default {
    props:{
        videoName: String,
        channelName: String,
        views: Number,
        upload: String,
        videoThumb: String,
        duration: String,
    },
    components: {
      DotsIcon,
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
  // max-width: auto;
  // max-height: 252px;
  align-items: center;
  margin: 0 .6rem 1rem .6rem;
  cursor: pointer;

  .thumb {
    margin-left: .2rem;
    img {
      width: 100%;
      height: auto;
      object-fit: cover;
    }
    .duration{
      background-color: rgba(0,0,0,.6);
      color: var(--white);
      padding: .2rem;
      float: right;
      margin: 0 .2rem 0 0;
      width: fit-content;
      font-size: 12px;
      font-weight: 500;
      border-radius: 4px;
      z-index: 2;
      position: relative;
      top: -1.7rem;
    }
  }
  .info {
    display: grid;
    grid-template-columns: 50px auto 24px;
    color: var(--gray);
    font-size: 14px;
    // width: 253px;
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
            overflow: hidden;
            color: var(--white);
            margin-bottom: .2rem;

            // Reticências no final do título
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
        }
        .channel-name{
            padding-bottom: .2rem;
            font-weight: 400;
            &:hover{
              color: var(--white);
            }
        }
        .video-info{
            font-weight: 400;
        }
    }
    .options{
      display: none;
    }
  }
}
.preview-container:hover{
  .options{
    display: block;
    &:hover{
      color: var(--white);
    }
  }
}
</style>