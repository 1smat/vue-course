<template>
  <form @submit.prevent>
    <h4>Create post</h4>
    <input
      v-model="post.title"
      class="input"
      type="text"
      name=""
      id=""
      placeholder="Post title"
    />
    <input
      v-model="post.body"
      class="input"
      type="text"
      placeholder="Description"
    />
    <button class="btn" @click="createPost">Create Post</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        id: '',
        title: '',
        body: '',
      },
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now()
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: '',
      }
    },
  },
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
form {
  margin-top: 20px;
}

.input {
  padding: 8px;
  margin: 8px;
  width: 100%;
}
.btn {
  border: none;
  padding: 12px;
  background-color: lightseagreen;
  color: white;
  border-radius: 4px;
}
.btn:hover {
  opacity: 0.8;
}
</style>
