<template>
  <div class="container">
    <div class="research">
      <AppResearch @searchClic="outputDate($event)"/>
    </div>
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
  computed: {
    cdFilter() {
      const filterArray = this.coverCd.filter((item) => {
        return item.genre.toLowerCase().includes(this.wordResearch)
      })
      return filterArray
    }
  },

  methods: {
    outputDate(word) {
      this.wordResearch = word.toLowerCase();
    }
  },
  data: function(){
    return {
      coverCd:[],
      wordResearch:"",
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