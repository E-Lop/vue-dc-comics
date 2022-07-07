<template>
  <section>
    <div class="bg_image"></div>
  </section>
</template>

<script>
export default {
  name: 'MyBanner',
};
</script>

<style lang="scss" scoped>
section {
  height: 300px;
  //   background-color: lightcoral;
}
.bg_image {
  height: 100%;
  background-image: url(../assets/img/jumbotron.jpg);
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
