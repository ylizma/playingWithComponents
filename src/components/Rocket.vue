<template>
  <div class="card col-4 ">
    <img :src="rocket.image" class="card-img-top" height="300px" :alt="rocket.name" />
    <div class="card-body">
      <h5 class="card-title"> {{rocket.name}} </h5>
      <p
        class="card-text"
      > {{rocket.description}} </p>
    </div>
    <button @click="removeRocket(rocket)" type="button" class="btn btn-danger">Delete</button>
  </div>
</template>

<script>
export default {
  props: ['rocket','removeRocket']
};
</script>

<style lang="scss" scoped>
</style>