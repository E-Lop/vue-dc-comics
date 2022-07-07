<template>
  <div>
    <!-- FOOTER TOP -->
    <section class="footer-top">
      <div class="container">
        <div class="content_at_top">
          <!-- colonna sx footer top -->
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
          <!-- colonna dx footer top -->
          <div class="col_dx">
            <img
              src="../assets/img/dc-logo-bg.png"
              alt="logo grande DC Comics"
            />
          </div>
        </div>
      </div>
    </section>
    <!-- FOOTER BOTTOM -->
    <section class="footer-bottom">
      <div class="container">
        <div class="content_at_bottom">
          <!-- colonna sx footer bottom -->
          <div class="col_sx_social">
            <span>SIGN-UP NOW!</span>
          </div>
          <!-- colonna dx footer bottom -->
          <div class="col_dx_social">
            <span>FOLLOW US</span>
            <ul>
              <li v-for="(element, index) in footerSocialSites" :key="index">
                <a :href="element.link">
                  <img :src="element.image" alt="element.name" />
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
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
      footerSocialSites: [
        {
          image: require('../assets/img/footer-facebook.png'),
          name: 'Facebook',
          link: '#',
        },
        {
          image: require('../assets/img/footer-twitter.png'),
          name: 'Twitter',
          link: '#',
        },
        {
          image: require('../assets/img/footer-youtube.png'),
          name: 'Youtube',
          link: '#',
        },
        {
          image: require('../assets/img/footer-pinterest.png'),
          name: 'Pinterest',
          link: '#',
        },
        {
          image: require('../assets/img/footer-periscope.png'),
          name: 'Periscope',
          link: '#',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../style/variables';
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
    height: 100%;
    object-fit: cover;
    object-position: center;
    overflow: hidden;
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
  background-color: #303030;
}
.content_at_bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.col_sx_social {
  width: 20%;
  color: white;
  padding: 25px 0;
  span {
    padding: 10px 10px;
    border: 1px solid $main_color;
  }
}
.col_dx_social {
  width: 80%;
  text-align: end;
  display: flex;
  align-items: center;
  justify-content: end;
  span {
    color: $main_color;
  }
  ul {
    display: flex;
    li {
      margin-left: 20px;
    }
  }
}
</style>
