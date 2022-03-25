<template>
  <main>
    <div class="container">
      <div class="delay-data text-center" v-if="arrDischi == null">
        <div>CARICAMENTO</div>
        <img class="loading" src="../assets/img/loading.png" alt="loading">
      </div>
      <div v-else class="row d-flex justify-content-center align-items-stretch g-3">

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
 props: {
   genderSelezionato: String,
 },
 components: {
   BoxDisco 
  },
  created () {
    setTimeout(() => {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) => {
      this.arrDischi = response.data.response;
    });
    }, 3000);
  } 
}
</script>

<style scoped lang="scss">
@import "../../node_modules/bootstrap/scss/functions";
@import "../../node_modules/bootstrap/scss/variables";
$secondary: #1e2d3b;

main {
  min-height: calc(100vh - 5rem);
  background-color: $secondary;
    .row {
      padding-top: 30px;
      padding-bottom: 40px;
    }
}
.delay-data {
  width: 100%;
  height: calc(100vh - 5rem);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  div {
    color: white;
    font-size: 35px;
    font-style: italic;
  }
}
.loading {
  width: 60px;
  font-size: 60px;
  animation-name: loading;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
@keyframes loading {
    0% {
        transform: rotate(1turn);
    }
}
</style>