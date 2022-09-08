<template>
  <div :style="{ fontSize: postFontSitze + 'em' }">
    <h1>My journey becoming a Frontend Web Developer</h1>
    <BlogTeaserList>
      <BlogPost
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        @enlarge-text="postFontSitze += 0.1"
      />
      <BlogPost title="Test Blog 4"></BlogPost>
      <template v-slot:show-number-of-posts
        >Number of posts: {{ posts.length }}</template
      >
    </BlogTeaserList>
  </div>
</template>

<script>
import BlogPost from "@/components/BlogPost.vue";
import BlogTeaserList from "@/components/BlogTeaserList.vue";

export default {
  name: "App",
  components: { BlogPost, BlogTeaserList },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "Test Blog 1",
        },
        {
          id: 2,
          title: "Test Blog 2",
        },
        {
          id: 3,
          title: "Test Blog 3",
        },
      ],
      postFontSitze: 1,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
