<template>
  <div class="container-single-disc col-6 col-md-4 col-lg-3 col-xl-2 text-center me-3 d-flex justify-content-center">
    <div class="box-single-disc">
        <img class="img-poster img-fluid" :src="dataDischi.poster" :alt="dataDischi.title">
        <h3 class="mt-3">{{ dataDischi.title.toUpperCase() }}</h3>
        <div class="box-author">{{ dataDischi.author }}</div>
        <div class="box-year">{{ dataDischi.year }}</div>
    </div>
  </div>
</template>

<script>
export default {
name: 'BoxDisco',
props: {
    dataDischi: Object
}
}
</script>

<style scoped lang="scss">
@import "../../node_modules/bootstrap/scss/functions";
@import "../../node_modules/bootstrap/scss/variables";
$success: #2e3a46;

.container-single-disc {
  background-color: $success;
  padding-bottom: 15px;
  padding-top: 30px;
    .box-single-disc {
      width: 170px;
      font-size: 15px;
        .img-poster {
          width: 170px;
        }
        h3 {
          font-size: 24px;
          color: white;
        }
        div {
          color: $gray-600;
        }
    }
}

</style>