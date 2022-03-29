<template>
  <div>
    <div>Likes: <b>{{likes}}</b></div>
    <div>DisLikes: <b> {{dislikes}}</b></div>
    <div>
      <button type="button" @click="add">like</button>
      <button type="button" v-on:click="dis">dislike</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      likes: 0,
      dislikes: 0
    }

  },
  methods: {
    add(){
      ++this.likes
    },
    dis(){
      ++this.dislikes
    },
  }
}
</script>

<style scoped>

</style>