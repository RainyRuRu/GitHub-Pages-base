<template>
  <div class="category">
    <div v-for="article in $route.meta" class="category__card-wrap" :key="article.directory">
      <Card
        :title="article.title"
        :imageUrl="article.image.url"
        :imageSite="article.image.site"
        :imageLink="article.image.link"
        :star="article.star"
        :short="article.short"
        :tags="article.tags"
        :time="article.time"
        :detail="article.detail"
      />
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue';

export default {
  name: 'category',
  components: {
    Card,
  },
};
</script>

<style lang="scss">
.category {
  padding: 15px 2%;
}

.category__card-wrap {
  display: inline-block;
  padding: 1%;
  width: 48%;
}
</style>
