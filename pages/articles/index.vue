<template>
  <section class="container mx-auto px-6 lg:px-32">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter&display=swap"
      rel="stylesheet"
    />
    
    <NavBar />
    <h1 class="font-body font-bold text-2xl mt-10">Articles</h1>
    <p class="font-blog">
      I generally write about software developement, exciting web technologies
      and new ways to look at coding and programming in general.
    </p>
    <BlogItem v-for="article in articles" :key="article.id" :title='article.title' :description='article.description' :path='article.path' />

  </section>
</template>

<script>
export default {
  async asyncData(context) {
    const { $content } = context
    const articles = await $content('articles').fetch()
    // console.log(articles[0].title)
    return { articles }
  },
}
</script>

<style>
</style>