<template>
  <div class="d-flex flex-column mt-4">
    <v-card
      class="mb-10 rounded-lg"
      v-for="post in posts"
      :key="post.id"
      max-width="500"
      @click="nuxtLink('/articles/' + post.id)"
    >
      <v-card-title>
        {{ post.title.rendered }}
      </v-card-title>
      <v-card-text v-if="post._embedded['wp:featuredmedia']">
        <div class="rounded overflow-hidden">
          <v-img
            :src="post._embedded['wp:featuredmedia'][0].source_url"
            max-height="200"
          />
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    // eslint-disable-next-line no-undef
    const wpSiteDomain = process.client
      ? process.env.wordpressApiUrl
      : 'wordpress'
    const posts = await $axios.$get(
      `http://${wpSiteDomain}/wp-json/wp/v2/posts/?_embed`
    )
    return { posts }
  },
  layout: 'blogs',
  methods: {
    nuxtLink(path) {
      this.$router.push({ path })
    },
  },
}
</script>

<style scoped></style>
