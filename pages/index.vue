<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        raphael
      </h1>
      <h2 class="subtitle">
        My grand Nuxt.js project
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
        <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  components: {
  },
   async asyncData ({ app, store, params }) {
    return { articles: await app.$wp.posts().perPage(10) }
  }
}
</script>

<style>

</style>
