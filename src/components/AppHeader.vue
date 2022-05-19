<template>
  <header class="header">
      <img src="../assets/logo.svg" alt="logo spotify">
  </header>
</template>

<script>
export default {
    name: "AppHeader",
}
</script>

<style>
    .header{
        padding: 0.5em;
        background-color: #2e3a46;
        height: 4em;
        width: 100%;
        display: flex;
        align-items: center;   
    }
    header img {
        height: 40px;
        }
</style>