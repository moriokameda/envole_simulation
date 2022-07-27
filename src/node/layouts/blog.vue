<template>
  <v-app>
    <Header></Header>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <Footer></Footer>
  </v-app>
</template>

<script>
import Header from '~/components/Header'
import Footer from '~/components/Footer'

export default {
  name: 'BlogLayout',
  components: { Header, Footer },
}
</script>
