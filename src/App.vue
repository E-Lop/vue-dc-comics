<template>
  <div id="app">
    <MyHeader />
    <main>
      <section class="main_content_section">
        <div class="container">Content goes here</div>
      </section>
      <section class="store_section">
        <div class="container">
          <ul>
            <li v-for="(icon, index) in icons" :key="index">
              <img :src="icon.image" alt="icon.name" />
              <a href="icon.link">{{ icon.name.toUpperCase() }}</a>
            </li>
          </ul>
        </div>
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
  data() {
    return {
      icons: [
        {
          image: require('./assets/img/buy-comics-digital-comics.png'),
          link: '#',
          name: 'Digital Comics',
        },
        {
          image: require('./assets/img/buy-comics-merchandise.png'),
          link: '#',
          name: 'DC Merchandise',
        },
        {
          image: require('./assets/img/buy-comics-subscriptions.png'),
          link: '#',
          name: 'Subscription',
        },
        {
          image: require('./assets/img/buy-comics-shop-locator.png'),
          link: '#',
          name: 'Comics Shop Locator',
        },
        {
          image: require('./assets/img/buy-dc-power-visa.svg'),
          link: '#',
          name: 'DC Power Visa',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import './style/common';
@import './style/variables';

.main_content_section {
  height: 100px;
  /* todo test */
  background-color: lightblue;
  line-height: 100px;
}
.store_section {
  background-color: $main_color;
  height: 150px;
}
.store_section {
  ul {
    display: flex;
    justify-content: space-between;
  }
}
.store_section {
  li {
    display: flex;
    align-items: center;
    a {
      color: white;
    }
  }
}
.store_section {
  img {
    width: 50px;
    height: 50px;
    object-fit: contain;
  }
}
.store_section {
  .container {
    height: 100%;
    line-height: 150px;
  }
}
</style>
