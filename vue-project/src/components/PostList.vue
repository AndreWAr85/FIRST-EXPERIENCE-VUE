<template>
  <div class="post" v-for="post in posts" :key="post.id">
    <div><strong>Nazwa: </strong>{{ post.title }}</div>
    <div><strong>Opis: </strong>{{ post.body }}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin: 5px;
  background: #e1e5e4;
}
</style>