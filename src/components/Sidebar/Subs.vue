<template>
  <div class="subs-container">
    <p class="subs">INSCRIÇÕES</p>
    <Channel hasNotification name="Alura Cursos Online" />
    <Channel name="Maikel Neris" />
    <Channel hasNotification name="Códgo Fonte TV" />
    <Channel hasNotification name="Fabio Akita" />
    <Channel hasNotification name="Filipe Deschamps" />
    <Channel name="Origamid" />
    <Channel name="Curso em Vídeo" />
    <Channel hasNotification name="Lucas Montano" />
    <Channel hasNotification name="Florin Pop" />
    <Channel name="Rocketseat" />
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
  width: 230px;
  display: flex;
  flex-direction: column;
  grid-area: SUBS;
  justify-content: space-around;
  padding: .6rem .2rem 0 .6rem;
  max-height: 100vh;
  cursor: pointer;
  border-bottom: solid 1px var(--hover);
  
  p.subs{
    color: var(--gray);
    align-self: flex-start;
    margin: .4rem 0 .4rem .6rem;
    font-size: 14px;
    font-weight: 600;
  }
}
</style>