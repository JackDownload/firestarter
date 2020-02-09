<template>
  <div>
    <ul v-for="(blogPost, index) in blogPosts" :key="index">
      <nuxt-link :to="`blog/${blogPost.slug}`">{{blogPost.title}} és {{blogPost.blogcategories}} és {{blogPost.categories}}</nuxt-link>
      <p>{{blogPost.description}}</p>
    </ul>
  </div>
</template>
<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    }
  }
}
</script>
