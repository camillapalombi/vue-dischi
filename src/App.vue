<template>
  <div id="app">
    <header-dischi @ricerca-rilanciata="setSelected" />
    <main-dischi :gender-selezionato="selectedGender" />
  </div>
</template>

<script>
import HeaderDischi from '../src/components/HeaderDischi.vue';
import MainDischi from '../src/components/MainDischi.vue';

export default {
  name: 'App',
  data () {
    return {
        selectedGender: '',
    }
},
  components: {
    HeaderDischi,
    MainDischi
  },
  methods: {
    setSelected(argomentoEvento) {
      this.selectedGender = argomentoEvento;
      console.log(this.selectedGender)
    }
  }
}
</script>

<style lang="scss">

@import "~bootstrap/scss/bootstrap";

</style>
