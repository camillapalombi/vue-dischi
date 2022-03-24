<template>
  <main>
    <div class="container">
      <div v-if="arrDischi == null">Dischi in caricamento, ATTENDI!</div>
      <div v-else class="row d-flex justify-content-center g-3">

        <box-disco
        v-for="dischi in arrDischi"
        :key="dischi.title"
        :data-dischi="dischi" />

      </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import BoxDisco from './BoxDisco.vue';

export default {
 name: 'MainDischi',
 data () {
   return {
      arrDischi: null,
   }
 },
 components: {
   BoxDisco 
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      console.log(response)
      this.arrDischi = response.data.response;
      console.log(this.arrDischi)
    })
  } 
}
</script>

<style scoped lang="scss">
@import "../../node_modules/bootstrap/scss/functions";
@import "../../node_modules/bootstrap/scss/variables";
$secondary: #1e2d3b;

main {
  background-color: $secondary;
}
</style>