<template>
  <post-form @create="createPost" />
  <post-list v-bind:posts="posts" />
</template>

<script>
import PostForm from './PostForm.vue'
import PostList from './PostList.vue'
export default {
  components: { PostForm, PostList },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: 'Post 1',
          body: 'Lorem ipsum dolor sit amet consectetur, adipisicing 1',
        },
        {
          id: 2,
          title: 'Post 2',
          body: 'Lorem ipsum dolor sit amet consectetur, adipisicing 2',
        },
        {
          id: 3,
          title: 'Post 3',
          body: 'Lorem ipsum dolor sit amet consectetur, adipisicing 3',
        },
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
    },
    getInputValue(event) {
      this.title = event.target.value
    },
  },
}
</script>

<style scoped></style>
