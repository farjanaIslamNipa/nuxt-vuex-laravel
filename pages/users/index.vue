<template>
  <div>
    <h1>user home page</h1>
    <input type="text" v-model="id" >
    <button @click="loadUser">Load User</button>
  </div>
</template>

<script>
  export default {
    name: 'UsersPage',
    layout: 'default',
    data() {
      return {
        id: ''
      }
    },
    methods: {
      loadUser() {
        this.$router.push(`/users/${this.id}`)
      }
    },
  }
</script>

<style scoped>

</style>