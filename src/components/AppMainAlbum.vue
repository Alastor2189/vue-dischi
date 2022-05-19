<template>
  <div class="container">
    <div class="row row-cols-5">
        <div class="card">
          <AppCd/>
        </div>
    </div>    
  </div>
</template>

<script>
import AppCd from "./AppCd.vue";
export default {
  name: "AppMainAlbum",
  components: {
    AppCd,
  }
}
</script>

<style lang="scss" scoped>

.card{
  width: calc(100% / 5 - 1em);
}

</style>