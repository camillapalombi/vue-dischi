<template>
  <header>
      <img class="img-fluid" src="../assets/img/spotify-logo.png" alt="Spotify Logo">

      <gender-select @select="rilanciaSelect" />

  </header>
</template>

<script>
import GenderSelect from './GenderSelect.vue';
export default {
    name: 'HeaderDischi',
    components: {
        GenderSelect
    },
    methods: {
        rilanciaSelect(argomento) {
            this.$emit('ricerca-rilanciata', argomento)
        }
    }
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
</style>