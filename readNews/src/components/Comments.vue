<template>
  <div id="">
    <div v-for="post in postsFeed" >
      <div v-show="post['.key'] == id" class="jumbotron">
      <h2 class="display-3">{{post.description}}</h2><br>
      <img :src="post.photo" alt="" @click="getID (post['.key'])" width="300px"><br>
      <hr class="my-4">
      {{post.comment}}
    </div>
    </div>
  </div>
</template>


<script>

export default {
  props: ['id','posts'],
  data () {
    return {

    }
  },
  methods: {

},
computed: {
  postsFeed () {
    console.log(this.posts)
    return this.posts.reverse()
  }
}
}
</script>

<style>
.border{
  width: 10%;
  height: 40%;
}
</style>
