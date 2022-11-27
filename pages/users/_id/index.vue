<template>
  <div>
    <h2>This is user {{ $route.params.id }}</h2>
  </div>
</template>

<script>
  export default {
    name: 'SingleUser',

    validate({ params }) {
        return /^\d+$/.test(params.id);
      }
  }

</script>

<style scoped>

</style>