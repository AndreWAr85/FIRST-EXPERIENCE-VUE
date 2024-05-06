<template>
  <form @submit.prevent>
    <h4>Tworzenie komentarzy</h4>

    <input
      v-bind:vaue="poat.title"
      @input="poast.title = $event.target.value"
      class="input"
      type="text"
      placeholder="Nazwa"
    />

    <input
      v-bind:vaue="post.body"
      @input="poast.body = $event.target.value"
      class="input"
      type="text"
      placeholder="Opis postu"
    />
    <button class="btn" @click="createPost">Stwórz</button>
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