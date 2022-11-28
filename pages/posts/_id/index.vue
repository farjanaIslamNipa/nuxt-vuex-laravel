<template>
  <div class="container">
    <h3 class="mt-4">{{ post.title }}</h3>
    <p>{{ post.body }}</p>
    <nuxt-link :to="{name: 'posts'}" class="btn btn-info fw-bold text-white">Go Back</nuxt-link>
  </div>
</template>

<script>
import axios from 'axios';

  export default {
    name: 'SinglePost',
    head(){
    return {
      title: this.post.title
    }
  },
    data() {
      return {
        post: ''
      }
    },

    async asyncData({ params }){
      let {data} = await axios.get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
      return {post: data}
    }
  }
</script>

<style scoped>
  
</style>