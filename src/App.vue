<template>
  <div class="app">
    <h4 class="app__title">Create post</h4>
    <Post-form />
    <Post-list :posts="posts"/>
  </div>
</template>

<script>
import PostList from '@/components/PostList'
import PostForm from '@/components/PostForm'

export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1,title: 'JS Post',body: 'Lorem ipsum dolor sit amet consectetur'},
        {id: 2,title: 'JS Post 2',body: 'Lorem ipsum dolor sit amet consectetur'},
        {id: 3,title: 'JS Post 3',body: 'Lorem ipsum dolor sit amet consectetur'},
        {id: 3,title: 'JS Post 4',body: 'Lorem ipsum dolor sit amet consectetur'},
      ],
    }
  },
  methods: {
    createPost(post){
      this.posts.push(post)
    },
  }
}
</script>

<style lang="scss">
* {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app{
  padding: 20px;

  &__title {
    margin-bottom: 15px;
  }

  &__post {
    border: 2px solid #ccc;
    border-radius: 8px;
    margin-bottom: 15px;
    padding: 10px 15px;
    &:last-child {
      margin-bottom: 0;
    }
  }
}







</style>