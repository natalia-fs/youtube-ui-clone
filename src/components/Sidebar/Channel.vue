<template>
  <div class="item-channel">
    <div class="channel-thumb"></div>
    <div class="channel-info">
      <p class="name">{{name}}</p>
      <div class="notification" v-if="hasNotification"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    hasNotification: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.item-channel {
  display: grid;
  grid-template-columns: 42px auto;
  flex-direction: row;
  align-items: center;
  font-weight: 400;
  font-size: 14px;
  width: 230px;
  height: 40px;
  padding: 0 1.4rem;
  p {
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
  }
  &:hover {
    background-color: var(--hover);
  }
  color: var(--icon-secondary);
  &.active {
    color: var(--white);
    background-color: var(--hover);
    font-weight: 600;
  }
  .channel-thumb {
    width: 24px;
    height: 24px;
    background-color: var(--white);
    border-radius: 50%;
  }
  .channel-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    .notification {
      background-color: #3ea6ff;
      width: 4px;
      height: 4px;
      border-radius: 50%;
    }
  }
}
</style>