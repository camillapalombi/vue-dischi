<template>
  <div class="col-6 col-md-4 col-lg-2 text-center me-3">
      <div class="container-single-disc">
        <img class="img-poster img-fluid" :src="dataDischi.poster" :alt="dataDischi.title">
        <h2>{{ dataDischi.title }}</h2>
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
.container-single-disc {
    font-size: 15px;
    color: white;
}

</style>