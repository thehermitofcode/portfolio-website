<template>
  <article class="container mx-auto px-6 lg:px-32">
    <NavBar />
    <h1 class="font-body font-bold text-2xl mt-10">{{ article.title }}</h1>
    <div class="font-blog text-sm mt-2">
        <p>By {{ article.author }}</p>
        <p class="text-gray-500">{{ article.createdAt | formatDate }}</p>
    </div>
    <div class="prose">
    <!-- <nuxt-content class="mt-6 font-blog" :document="article"></nuxt-content> -->
    </div>
  </article>
</template>

<script>
import { format } from 'date-fns'
export default {
    filters: {
        formatDate() {
            return format(new Date(), 'dd MMM yyyy')
        }
    },
  async asyncData({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()
    return { article }
  },
}
</script>

<style>
</style>