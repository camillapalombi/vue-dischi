<template>
  <header>
      <img src="../assets/img/spotify-logo.png" alt="Spotify Logo">
  </header>
</template>

<script>
export default {
    name: 'HeaderDischi',
}
</script>

<style scoped lang="scss">
@import "../../node_modules/bootstrap/scss/functions";
@import "../../node_modules/bootstrap/scss/variables";
$primary: #2e3a46;

header {
    height: 4rem;
    background-color: $primary;
    display: flex;
    align-items: center;
        img {
            width: 45px;
            margin-left: 20px;
        }
}
</style>