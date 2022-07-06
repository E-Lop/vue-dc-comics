<template>
  <div>
    <div class="container">
      <section>
        <div class="col-sx">
          <div class="image-logo">
            <img src="../assets/img/dc-logo.png" alt="Logo DC Comics" />
          </div>
        </div>
        <div class="col-dx">lista di sezioni del sito</div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyHeader',
  data() {
    return {
      sitesection: 'characters',
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.image-logo {
  width: 60px;
}
</style>
