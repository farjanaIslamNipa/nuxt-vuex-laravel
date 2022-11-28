<template>
  <div class="container">
    <h1 class="mt-4 mb-5">Making API request VUE way</h1>
    <div class="row">
      <div v-for="post in posts" :key="post.id" class="col-md-4 mb-4">
        <PostCard :post="post" />
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
  export default {
    name: 'PostIndex',
    layout: 'default',
    head(){
    return {
      title: 'Posts'
    }
  },
    data() {
      return {
        posts: ''
      }
    },
    async asyncData(){
      let { data } = await axios.get('https://jsonplaceholder.typicode.com/posts')
      return {posts: data}
    },
    // head: {
    //   title: 'Posts'
    // }
    // mounted (  ) {
    //   axios.get('https://jsonplaceholder.typicode.com/todos')
    //   .then(response => {
        
    //     this.posts = response.data
    //     console.log(this.posts, 'data')
    //   })
    //   .catch(error => {console.log(error)})
    // },
  }
</script>

<style scoped>

</style>