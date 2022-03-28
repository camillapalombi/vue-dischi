<template>
  <div id="app">
    <header-dischi @ricerca-rilanciata="setSelected" @author-inserted="SetAuthorSrc"/>
    <main-dischi :gender-selezionato="selectedGender" :str-search-author="strSearchAuthor"/>
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
        strSearchAuthor: '',
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
    },
    SetAuthorSrc(authorArguments) {
      console.log(authorArguments)
      this.strSearchAuthor = authorArguments;
    }
  }
}
</script>

<style lang="scss">

@import "~bootstrap/scss/bootstrap";

</style>
