<template>
  <div class="comic_book_card">
    <img :src="comicsDetails.thumb" alt="comicsDetails.series" />
    <h2>{{ comicsDetails.series }}</h2>
  </div>
</template>

<script>
export default {
  name: 'ComicsCard',
  props: {
    comicsDetails: Object,
  },
};
</script>

<style lang="scss" scoped>
.comic_book_card {
  padding: 10px;
  width: calc((100% / 6) - 5px);
  margin: 2px;
  //   todo test
  background-color: white;
}
</style>
