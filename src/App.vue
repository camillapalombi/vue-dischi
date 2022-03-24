<template>
  <div id="app">
    <header-dischi />
    <main-dischi />
  </div>
</template>

<script>
import HeaderDischi from '../src/components/HeaderDischi.vue';
import MainDischi from '../src/components/MainDischi.vue';

export default {
  name: 'App',
  components: {
    HeaderDischi,
    MainDischi
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
