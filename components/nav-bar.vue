<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">NuxtApp</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav">
            <nuxt-link class="nav-link active" aria-current="page" to="/">Home</nuxt-link>
            <nuxt-link class="nav-link" to="/users">Users</nuxt-link>
            <nuxt-link class="nav-link" to="/posts">Posts</nuxt-link>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: 'NavBar'
  }
</script>

<style scoped>

</style>