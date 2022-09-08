<template>
  <div class="blog-post">
    <h2>{{ title }}</h2>
    <button @click="$emit('enlarge-text')">Enlarge text</button>
  </div>
</template>

<script>
export default {
  name: "BlogPost",
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
*,
*::before,
*::after {
  box-sizing: border-box;
}
</style>
