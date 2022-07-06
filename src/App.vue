<template>
  <div id="app">
    <MyHeader />
    <main>
      <section>Content goes here</section>
      <section>seconda section con sfondo blu</section>
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
</style>
