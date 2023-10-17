
<template>
  <div  class="app__post">
      <div><strong>name: </strong>{{ post.title }}</div>
      <div><strong>description: </strong>{{ post.body }}</div>
    </div>
</template>
<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>
<style></style>