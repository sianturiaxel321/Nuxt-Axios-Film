<template>
  <div class="col-md-4">
    <div
      class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative"
    >
      <div class="article-img col-12 d-none d-lg-block">
        <img :src="article.options.image" alt="#" />
      </div>

      <div class="col-12 p-4 d-flex flex-column position-static">
        <h4 align="justify">{{ article.options.name }}</h4>
        <p class="card-text mb-auto">{{ article.options.genre }}</p>
        <p class="card-text mb-auto">{{ article.rating }}</p>
        <a :href="article.downloadLink" class="stretched-link" target="_blank"
          >Download Link</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    article: {
      type: Object,
    },
    options: {
      type: Object,
    },
  },
};
</script>

<style scoped>
.article-img img {
  width: 100%;
}
</style>
