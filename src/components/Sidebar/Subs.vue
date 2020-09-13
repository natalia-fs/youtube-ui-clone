<template>
  <div class="subs-container">
    <p class="subs">INSCRIÇÕES</p>
    <Channel hasNotification name="Alura Cursos Online" />
    <Channel name="Rocketseat" />
    <Channel hasNotification name="Códgo Fonte TV" />
    <Channel hasNotification name="Filipe Deschamps" />
    <Channel hasNotification name="Fabio Akita" />
    <Channel name="Maikel Neris" />
    <Channel name="Origamid" />
    <Channel hasNotification name="Florin Pop" />
    <Channel hasNotification name="Lucas Montano" />
    <Channel name="Curso em Vídeo" />
    <Channel hasNotification name="freeCodeCamp.org" />
  </div>
</template>

<script>
import Channel from './Channel'
export default {
  components: {
    Channel,
  }
}
</script>

<style lang="scss">
.subs-container{
  display: flex;
  flex-direction: column;
  grid-area: SUBS;
  align-items: center;
  justify-content: center;
  padding-top: .8rem;
  max-height: calc(100vh - 56px - 147px - 247px);
  overflow-y: scroll;
  cursor: pointer;
  border-bottom: solid 1px var(--hover);
  &::-webkit-scrollbar{
    width: 8px;
  }
  &::-webkit-scrollbar-thumb{
    background-color: var(--hover);
    border-radius: 4px;
  }
  p.subs{
    color: var(--gray);
    padding-right: 6.6rem;
    padding-bottom: .4rem;
    font-size: 14px;
  }
}
</style>