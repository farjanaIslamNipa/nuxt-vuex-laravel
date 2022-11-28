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
      },
    head(){
    return {
      title: 'User'
    }
  },
  }

</script>

<style scoped>

</style>