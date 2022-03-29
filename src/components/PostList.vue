<template>
    <div class="post" v-bind:key="post" v-for="post in posts">
    <div> <strong>Post name : </strong> {{post.title}}</div>
    <div> <strong> Post description :</strong> {{post.body}} </div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.post {
  margin-top: 12px;
  border: 2px solid;
  padding: 10px;
}
</style>