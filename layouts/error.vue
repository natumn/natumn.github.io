<template>
  <div class="container">
    <h1 class="title" v-if="error.statusCode === 404">404: Not found page.</h1>
    <h1 class="subtitle" v-else>エラーが発生しました</h1>
    <div class="links">
      <nuxt-link to="/">ホーム</nuxt-link>
    </div>
  </div>
</template>
<script>
export default {
  props: ['error'],
  layout: 'blog'
}
</script>
<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
  display:block;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
  display:block;
}
</style>
