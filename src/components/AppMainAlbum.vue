<template>
  <div class="container">
    <div class="row row-cols-5">
          <AppCd v-for="(item, index) in coverCd" :key="index" :album="item"/>
    </div>    
  </div>
</template>

<script>
import AppResearch from "./AppResearch.vue";
import AppCd from "./AppCd.vue";
import axios from "axios"
export default {
  name: "AppMainAlbum",
  components: {
    AppCd,
    AppResearch,
  },
  data: function(){
    return {
      coverCd:[],
    };
  },
  created() {
    axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((resp) => {
      this.coverCd = resp.data.response;

    });
  }
};
</script>

<style lang="scss" scoped>



</style>