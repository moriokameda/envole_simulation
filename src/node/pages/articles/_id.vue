<template>
  <div>this is article detail page.
    <h2>{{ post.title.rendered }}</h2>
    <!-- eslint-disable-next-line vue/no-v-html -->
    <div v-html="post.content.rendered"></div>
  </div>
</template>

<script>
export default {
  async asyncData(context) {
    // eslint-disable-next-line no-undef
    const wpSiteDomain = process.client ? process.env.wordpressApiUrl : 'wordpress'
    const post = await context.$axios.$get(`http://${wpSiteDomain}/wp-json/wp/v2/posts/${context.params.id}`)
    // const post = await context.$axios.$get(`http://wordpress/wp-json/wp/v2/posts/${context.params.id}`)
    return { post }
  }
}
</script>

<style scoped>

</style>
