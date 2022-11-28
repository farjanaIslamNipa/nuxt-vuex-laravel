<template>
<div class="card h-100">
  <div class="card-body">
    <h6>Post Id: #{{post.id}}</h6>
    <h5 class="card-title mb-4">{{ post.title }}</h5>
    <nuxt-link :to="{name: 'posts-id', params:{id: post.id}}" class="btn btn-info fw-bold text-white">Read More</nuxt-link>
  </div>
</div>
</template>

<script>
  export default {
    name: 'PostCard',
    props: {
      post: Object
    }
  }
</script>

<style scoped>

</style>