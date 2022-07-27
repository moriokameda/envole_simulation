<template>
  <div>
    <div class="d-flex mb-5">
      <div class="mr-4">
        <div class="caption">{{ formatDate(post.date, 'YYYY') }}</div>
        <div class="font-weight-bold">{{ formatDate(post.date, 'MM/DD') }}</div>
      </div>
      <v-divider vertical></v-divider>
      <div class="ml-4 d-flex flex-column justify-center">
        <h2>{{ post.title.rendered }}</h2>
      </div>
    </div>

    <v-card class="rounded-lg" max-width="400">
      <v-card-title>
        <div class="mr-4">目次</div>
        <v-divider vertical></v-divider>
      </v-card-title>
      <v-card-text>
        <!-- eslint-disable-next-line vue/no-v-html -->
        <div v-html="tableOfContents(post)"></div>
      </v-card-text>
    </v-card>

    <!-- eslint-disable-next-line vue/no-v-html -->
    <div v-html="postBody(post)"></div>
  </div>
</template>

<script>
export default {
  async asyncData(context) {
    // eslint-disable-next-line no-undef
    const wpSiteDomain = process.client
      ? process.env.wordpressApiUrl
      : 'wordpress'
    const post = await context.$axios.$get(
      `http://${wpSiteDomain}/wp-json/wp/v2/posts/${context.params.id}`
    )
    // const post = await context.$axios.$get(`http://wordpress/wp-json/wp/v2/posts/${context.params.id}`)
    return { post }
  },
  layout: 'blog',
  methods: {
    formatDate(dateString, format) {
      const date = new Date(dateString)

      format = format.replace(/YYYY/, date.getFullYear())
      format = format.replace(/MM/, date.getMonth() + 1)
      format = format.replace(/DD/, date.getDate())

      return format
    },
    tableOfContents(post) {
      // 目次にEasy Table of Contentsを使っている想定です
      const rendered = post.content.rendered
      const toc = rendered.substring(
        rendered.indexOf('<nav>'),
        rendered.indexOf('</nav>') + 6
      )

      return toc
    },
    postBody(post) {
      // 目次にEasy Table of Contentsを使っている想定です
      const rendered = post.content.rendered
      const body = rendered.split('</nav></div>')[1]

      return body
    },
  },
}
</script>

<style scoped></style>
