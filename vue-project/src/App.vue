

<template>
  <!--  <div>
    <div>
      Количество лайков:<strong>{{ likes }}</strong>
    </div>
    <div>
      Количество дизлайков:<strong>{{ dislikes }}</strong>
    </div>
    <div>
      <button v-on:click="addLikes">Likes</button>
      <button v-on:click="addDislikes">Dislikes</button>
    </div>
  </div>
  <div class="post">
    <div><strong>Nazwa:</strong>Post o JavaScript</div>
    <div><strong>Opis:</strong>JavaScript uniwersalny język progromowania</div>
  </div>
  <div class="post">
    <div><strong>Nazwa:</strong>Post o JavaScript</div>
    <div><strong>Opis:</strong>JavaScript uniwersalny język progromowania</div>
  </div>
  <div class="post">
    <div><strong>Nazwa:</strong>Post o JavaScript</div>
    <div><strong>Opis:</strong>JavaScript uniwersalny język progromowania</div>
  </div>
  </div>-->
  <div class="app">
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostForm from "./components/PostForm.vue";
import PostList from "./components/PostList.vue";
export default {
  components: {
    PostForm,
    PostList,
  },
  /*data() {
    return {
      likes: 0,
      dislikes: 2,
    };
  },*/
  data() {
    return {
      posts: [
        { id: 1, title: "Javascript 1", body: "Opis komentarza 1" },
        { id: 2, title: "Javascript 2", body: "Opis komentarza 2" },
        { id: 3, title: "Javascript 3", body: "Opis komentarza 3" },
        { id: 4, title: "Javascript 4", body: "Opis komentarza 4" },
      ],
    };
  },
  methods: {
    /* addLikes() {
      this.likes += 1;
    },
    addDislikes() {
      this.dislikes += 1;
    },*/
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>