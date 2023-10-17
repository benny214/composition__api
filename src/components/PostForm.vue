
<template>
  <div>
    <form @submit.prevent
      	  class="app__form">
      <input v-model="post.title"
             class="form__input" 
             type="text" 
             placeholder="name">
      <input v-model="post.body"
             class="form__input" 
             type="text" 
             placeholder="body">
      <button @click="createPost" 
              class="form__btn">Create</button>
    </form>
  </div>
</template>
<script>


export default {
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Data.now();
      this.emit('create', this.post);
      this.post = {
        title: '',
        body: ''
      }
    }
  }
}
</script>
<style lang="scss">
.app__form {
    margin-bottom: 15px;
    display: flex;
    flex-direction: column;
    gap: 15px;
    .form__input {
    width: 100%;
    border: 1px solid #ccc;
    padding: 10px 15px;
    border-radius: 8px;
  }

  .form__btn {
    padding: 10px 15px;
    border-width: 0;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.25s ease;
    align-self: flex-end;
    &:hover {
      background-color: #ccc;
      color: #fff;
    }
  }
}

  
</style>