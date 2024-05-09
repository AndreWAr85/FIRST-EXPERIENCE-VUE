<template>
  <form @submit.prevent="createPost">
    <h4>Tworzenie komentarzy</h4>
    <input v-model="post.title" class="input" type="text" placeholder="Nazwa" />
    <input v-model="post.body" class="input" type="text" placeholder="Opis" />
    <button class="btn">Stwórz</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>


<style scoped>
form {
  display: flex;
  flex-direction: column;
}
.btn {
  align-self: flex-end;
  color: #ffffff;
  margin: 5px;
  background: #46635d;
  border-radius: 5px;
  padding: 4px 6px;
}

.input {
  width: auto;
  border: 1px solid rgb(6, 70, 70);
  padding: 10px 15px;
  margin: 3px 5px;
  background: #dbf0ec;
}
</style>