<template>
  <article class="p-6 mx-auto prose prose-headings:font-light md:prose-lg lg:prose-xl max-w-4xl">
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    const page = await $content('home').fetch()
    return { page }
  }
}
</script>
