<template>
  <div id="app">
    <AppHeader/>
    <AppMainAlbum/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMainAlbum from './components/AppMainAlbum.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMainAlbum,
}
}
</script>

<style lang="scss">
    @import "./style/common.scss"
</style>

