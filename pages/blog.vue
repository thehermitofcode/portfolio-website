<template>
  <div>{{ articles }}</div>
</template>

<script>
export default {
  async asyncData(context) {
    const { $content } = context
    const articles = await $content('blog').fetch()
    return { articles }
  },
}
</script>

<style>
</style>