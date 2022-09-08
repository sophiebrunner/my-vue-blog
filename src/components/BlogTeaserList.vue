<template>
  <div class="blog-teaser-list">
    <h2>Latest blog posts</h2>
    <div class="posts">
      <slot></slot>
    </div>
    <slot name="show-number-of-posts"></slot>
  </div>
</template>

<script>
export default {
  name: "BlogTeaserList",
};
</script>

<style scoped>
.posts {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}
</style>
