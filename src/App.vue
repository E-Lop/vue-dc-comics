<template>
  <div id="app">
    <div class="container">
      <MyHeader />
    </div>
    <main>
      <div class="container">
        <section>Content goes here</section>
        <section>seconda section con sfondo blu</section>
      </div>
    </main>
    <div class="container"><MyFooter /></div>
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
</style>
