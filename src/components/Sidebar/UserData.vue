<template>
  <div class="user-data-container">
    <div class="item">
      <div class="icon">
        <LibraryIcon :size="22"/>
      </div>
      <p>Biblioteca</p>
    </div>
    <div class="item">
      <div class="icon">
        <HistoryIcon :size="22"/>
      </div>
      <p>Histórico</p>
    </div>
    <div class="item">
      <div class="icon">
        <VideosIcon :size="22"/>
      </div>
      <p>Seus vídeos</p>
    </div>
    <div class="item">
      <div class="icon">
        <ClockIcon :size="22"/>
      </div>
      <p>Assistir mais tarde</p>
    </div>
    <div class="item">
      <div class="icon">
        <ThumbIcon :size="22"/>
      </div>
      <p>Vídeos marcados com gostei</p>
    </div>
    <div class="item">
      <div class="icon">
        <Playlist :size="22"/>
      </div>
      <p>Playlists</p>
    </div>
  </div>
</template>

<script>
import LibraryIcon from "vue-material-design-icons/PlayBoxMultiple";
import HistoryIcon from "vue-material-design-icons/History";
import VideosIcon from "vue-material-design-icons/PlayBoxOutline";
import ClockIcon from "vue-material-design-icons/Clock";
import ThumbIcon from "vue-material-design-icons/ThumbUp";
import Playlist from "vue-material-design-icons/PlaylistPlay";
export default {
  components: {
    LibraryIcon,
    HistoryIcon,
    VideosIcon,
    ClockIcon,
    ThumbIcon,
    Playlist,
  }
}
</script>

<style lang="scss" scoped>
.user-data-container{
  grid-area: USER;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
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
    p{
      display: inline-block;
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
    }
  }
}
</style>