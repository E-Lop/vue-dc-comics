<template>
  <div class="container">
    <div class="comics-list">
      <div class="comics-card">Superman</div>
      <div class="comics-card">Superman</div>
      <div class="comics-card">Superman</div>
      <div class="comics-card">Superman</div>
      <div class="comics-card">Superman</div>
      <div class="comics-card">Superman</div>
      <div class="comics-card">Superman</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ComicsPage',
};
</script>

<style lang="scss" scoped>
.comics-list {
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  .comics-card {
    width: calc(100% / 6);
  }
}
</style>
