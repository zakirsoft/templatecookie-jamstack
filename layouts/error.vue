<template>
  <div class="error-section">
    <div class="container">
      <div class="text-center">
        <h2 class="mb-3"> Nothing Found! </h2>
        <nuxt-link :to="{ name: 'index'}" class="details--content__button">Go Home</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .error-section {
    padding: 20vh 0;
    background-image: url('~assets/images/newest-background.png');
    background-color: bisque;
  }
</style>
