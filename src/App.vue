<template>
  <div id="app">
    <!-- HEADER -->
    <MyHeader />
    <!-- MAIN -->
    <main>
      <!-- BANNER -->
      <MyBanner />
      <!-- PRODOTTI SELEZIONATI -->
      <section class="main_content_section">
        <ComicsPage />
        <!-- tasto load more -->
        <div class="load_more_btn">
          <a href="#">LOAD MORE</a>
        </div>
      </section>
      <!-- SEZIONE STORE -->
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
    <!-- FOOTER -->
    <MyFooter />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MyHeader from './components/MyHeader.vue';
import MyFooter from './components/MyFooter.vue';
import ComicsPage from './components/ComicsPage.vue';
import MyBanner from './components/MyBanner.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyFooter,
    ComicsPage,
    MyBanner,
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

/* Sezione principale prodotti selezionati */
.main_content_section {
  background-color: #1c1c1c;
  padding-top: 20px;
  padding-bottom: 10px;
}
.load_more_btn {
  width: 120px;
  margin: 0 auto;
  background-color: $main_color;
  text-align: center;
  padding: 5px 10px;
  a {
    font-size: 0.9rem;
    color: white;
  }
}

/* sezione con icone dello store */
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
    margin-right: 5px;
  }
}
.store_section {
  .container {
    height: 100%;
    line-height: 150px;
  }
}
</style>
