<template>
  <div id="app">
    <MyHeader />
    <main>
      <section .main_content_section>
        <div class="container">Content goes here</div>
      </section>
      <section .store_section>
        <div class="container">seconda section con sfondo blu</div>
      </section>
    </main>
    <MyFooter />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MyHeader from './components/MyHeader.vue';
import MyFooter from './components/MyFooter.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyFooter,
  },
};
</script>

<style lang="scss">
@import './style/common';
@import './style/variables';

.store_section {
  background-color: $main_color;
}
</style>
