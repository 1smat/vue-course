<template>
  <!-- <like-counter></like-counter> -->
  <LikeCounter />
  <post-component></post-component>
</template>
<script>
import LikeCounter from './components/LikeCounter.vue';
import PostComponent from './components/PostComponent.vue'
export default {
  components: { LikeCounter,
  PostComponent },

}
</script>

<style scoped>

</style>