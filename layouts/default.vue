<template>
  <v-app>
    <v-layout>
      <v-app-bar density="compact" absolute>
        <v-app-bar-title class="text-uppercase">
          gyo12.ru
        </v-app-bar-title>
        <v-spacer />
        <v-btn class="mr-3" text>
          Help
        </v-btn>

        <v-divider inset vertical />

        <v-btn
          class="mr-4 ml-5"
          color="primary"
          plain
        >
          <v-icon left icon="mdi-handshake-outline" />

          <a :href="link" target="_blank"><span>Tobias Reaper</span></a>
        </v-btn>
      </v-app-bar>
      <v-main>
        <v-sheet border>
          <nuxt-page />
        </v-sheet>
      </v-main>
    </v-layout>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      link: ''
    }
  },
  created () {
    this.link = process.env.MY_PAGE_VK // 'https://cdn.worldvectorlogo.com/logos/vk-com-logo.svg'
  }
}
</script>

<style scoped >
  a, a:visited, a:hover, a:focus{
    color:white;
    text-decoration: none;
  }
</style>
