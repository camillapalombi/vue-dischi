<template>
  <div>

    <select @change="$emit('select', selectedGender)" class="form-select" aria-label="Default select example" v-model="selectedGender">
        <option value="all">All</option>
        <option value="rock">Rock</option>
        <option value="pop">Pop</option>
        <option value="jazz">Jazz</option>
        <option value="metal">Metal</option>
    </select>
    

  </div>
</template>

<script>
export default {
name: 'GenderSelect',
data () {
    return {
        selectedGender: 'all',
    }
}
}
</script>

<style scoped lang="scss">
.form-select {
    width: 250px;
    margin-bottom: 15px;
    margin-right: 30px;
}
</style>