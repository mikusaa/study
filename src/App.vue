<template>
  <div id="app">
    <Postcard 
    v-for="post in list"
     :key="post.count" 
     :count="post.count" 
     :data="post.data"
    ></Postcard></div>
    
</template>

<script>
import Postcard from './components/postcard.vue'

export default {
  name: 'App',
  components: {
    Postcard
  },
  data(){
    return{
      list:[
        {
          count: 1000,
          date: "20210501",
        },
         {
          count: 2000,
          date: "20210401",
        },
        {
          count: 3000,
          date: "20210301",
        },
        {
          count: 4000,
          date: "20210201",
        },
        {
          count: 5000,
          date: "20210101",
        },
        {
          count: 6000,
          date: "20200501",
        }
      ]
    }
  }
}
</script>

<style>
</style>
