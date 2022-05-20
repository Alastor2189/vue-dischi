<template>
  <div class="search">
      <select name="" id="" v-model="research" @change="$emit('searchClic','research')">
            <option value="">All</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
      </select>
      
  </div>
</template>

<script>
export default {
    name: "AppResearch",
    data: function(){
         return {
            research:"",
        };
        
        },
        methods: {
            
        },
    
};
</script>

<style>

</style>