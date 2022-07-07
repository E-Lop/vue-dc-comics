<template>
  <div>
    <section class="footer-top">
      <div class="container">
        <div class="content_at_top">
          <div class="col_sx">
            <div class="sitemap_links">
              <h2>DC COMICS</h2>
              <ul>
                <li v-for="(element, index) in footerComics" :key="index">
                  <a href="element.link">{{ element.text }}</a>
                </li>
              </ul>
              <h2>SHOP</h2>
              <ul>
                <li v-for="(element, index) in footerShop" :key="index">
                  <a href="element.link">{{ element.text }}</a>
                </li>
              </ul>
              <h2>DC</h2>
              <ul>
                <li v-for="(element, index) in footerDC" :key="index">
                  <a href="element.link">{{ element.text }}</a>
                </li>
              </ul>
              <h2>SITES</h2>
              <ul>
                <li v-for="(element, index) in footerSites" :key="index">
                  <a href="element.link">{{ element.text }}</a>
                </li>
              </ul>
            </div>
          </div>
          <div class="col_dx">
            <img
              src="../assets/img/dc-logo-bg.png"
              alt="logo grande DC Comics"
            />
          </div>
        </div>
      </div>
    </section>
    <section class="footer-bottom">
      <div class="container">social</div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'MyFooter',
  data() {
    return {
      footerComics: [
        {
          text: 'Characters',
          link: '#',
        },
        {
          text: 'Comics',
          link: '#',
        },
        {
          text: 'Movies',
          link: '#',
        },
        {
          text: 'TV',
          link: '#',
        },
        {
          text: 'Games',
          link: '#',
        },
        {
          text: 'Videos',
          link: '#',
        },
        {
          text: 'News',
          link: '#',
        },
      ],
      footerShop: [
        {
          text: 'Shop DC',
          link: '#',
        },
        {
          text: 'Shop DC Collectibles',
          link: '#',
        },
      ],
      footerDC: [
        {
          text: 'Terms Of Use',
          link: '#',
        },
        {
          text: 'Privacy policy (New)',
          link: '#',
        },
        {
          text: 'Ad Choices',
          link: '#',
        },
        {
          text: 'Advertising',
          link: '#',
        },
        {
          text: 'Jobs',
          link: '#',
        },
        {
          text: 'Subscriptions',
          link: '#',
        },
        {
          text: 'Talent Workshops',
          link: '#',
        },
        {
          text: 'CPSC Certificates',
          link: '#',
        },
        {
          text: 'Ratings',
          link: '#',
        },
        {
          text: 'Shop Help',
          link: '#',
        },
        {
          text: 'Contact Us',
          link: '#',
        },
      ],
      footerSites: [
        {
          text: 'DC',
          link: '#',
        },
        {
          text: 'MAD Magazine',
          link: '#',
        },
        {
          text: 'DC Kids',
          link: '#',
        },
        {
          text: 'DC Universe',
          link: '#',
        },
        {
          text: 'DC Power Visa',
          link: '#',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
/* FOOTER TOP */
.footer-top {
  height: 300px;
  background-image: url(../assets/img/footer-bg.jpg);
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
}
.container {
  height: 100%;
}
.content_at_top {
  width: 100%;
  height: 100%;
  display: flex;
}
.col_sx {
  height: 100%;
  width: 60%;
  h2 {
    color: white;
    padding-top: 10px;
    padding-bottom: 10px;
  }
}
.col_dx {
  width: 40%;
  display: flex;
  align-items: center;
  img {
    overflow: hidden;
    align-self: center;
  }
}
.sitemap_links {
  height: 100%;
  padding-top: 20px;
  padding-bottom: 20px;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  a {
    color: #657b81;
  }
}
/* FOOTER BOTTOM */
.footer-bottom {
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
