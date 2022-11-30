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
import {mapGetters} from 'vuex';
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
        allPosts: ''
      }
    },
    computed: {
      ...mapGetters(['posts'])
    },
    async fetch({store}){
      let { data } = await axios.get('https://jsonplaceholder.typicode.com/posts')
      store.dispatch('setPosts', data)
    }
  }
</script>

<style scoped>

</style>