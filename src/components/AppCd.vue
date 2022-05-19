<template>
  <div class="cover-cd text-center p-3">
    <img class="" :src="album.poster" :alt="album.name">
    <div class="information">
        <h3 class="">
            {{ album.title }}
        </h3>
        
        <p> {{ album.author }}</p>
        <small>
            {{ album.year }}
        </small>
    </div>
  </div>
</template>

<script>
export default {
    name:"AppCd",
    props: {
        album:Object
    }
}
</script>

<style lang="scss" scoped>
.cover-cd{
    width: calc((100%/5) - 2em);
    padding: 2em;
    background-color: #2e3a46;
    margin: 8px;
}

    img{
        width: 90%;
        background-color: #2e3a46;
    }

    h3{
        text-transform: uppercase;
        font-size: 1.5em;
    }

    p, small{
        margin: 0;
        opacity: 0.4;

    }
</style>