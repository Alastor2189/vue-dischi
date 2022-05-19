<template>
  <div id="app">
    <AppHeader/>
    <div class="container p-5">
      <AppMainAlbum/>
    </div>
    
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMainAlbum from './components/AppMainAlbum.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMainAlbum
}
}
</script>

<style lang="scss">
    @import "./style/common.scss"
</style>

