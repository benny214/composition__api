
<template>
  <div>
    <div   
       class="app__post">
      <PostItem v-for="post in posts"
                :post="post"/>
    </div>
  </div>
  
</template>
<script>
import PostItem from '@/components/PostItem'
export default {
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>
<style></style>