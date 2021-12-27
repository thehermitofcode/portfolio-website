<template>
  <section class="mt-10">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Inter&display=swap"
      rel="stylesheet"
    />
    <h2 class="font-body text-lg font-bold tracking-normal">{{ title }}</h2>
    <div class="font-blog">
    <p class="text-base mt-1">{{ description }}</p>
    <a :href="slug" class="text-sm underline text-gray-500 mt-2 inline-block">Read this article</a>
    </div>
  </section>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: ''
        },
        description: {
            type: String,
            default: ''
        },
        slug: {
            type: String,
            default: ''
        },
    }
}
</script>

<style>
</style>