<template>
  <header>
      <img class="img-fluid" src="../assets/img/spotify-logo.png" alt="Spotify Logo">

      <select class="form-select" aria-label="Default select example">
        <option selected>Seleziona genere musicale</option>
        <option value="rock">Rock</option>
        <option value="pop">Pop</option>
        <option value="jazz">Jazz</option>
        <option value="metal">Metal</option>
    </select>

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
    height: 5rem;
    background-color: $primary;
    display: flex;
    justify-content: space-between;
    align-items: center;
        img {
            height: 40px;
            margin-left: 20px;
            margin-bottom: 15px;
        }
}

.form-select {
    width: 250px;
    margin-bottom: 15px;
    margin-right: 20px;
}
</style>