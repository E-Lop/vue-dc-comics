<template>
  <div>
    <div class="container">
      <section>
        <!-- parte sinistra con logo -->
        <div class="col-sx">
          <div class="image-logo">
            <img src="../assets/img/dc-logo.png" alt="Logo DC Comics" />
          </div>
        </div>
        <!-- parte destra con navigazione -->
        <div class="col-dx">
          <nav>
            <ul>
              <li v-for="(pippo, index) in sitesection" :key="index">
                <a :class="{ current: pippo.current }" :href="pippo.link">{{
                  pippo.name
                }}</a>
                <span class="underline"></span>
              </li>
            </ul>
          </nav>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyHeader',
  data() {
    return {
      sitesection: [
        {
          name: 'CHARACTERS',
          link: '#',
          current: false,
        },
        {
          name: 'COMICS',
          link: '#',
          current: true,
        },
        {
          name: 'MOVIES',
          link: '#',
          current: false,
        },
        {
          name: 'TV',
          link: '#',
          current: false,
        },
        {
          name: 'GAMES',
          link: '#',
          current: false,
        },
        {
          name: 'COLLECTIBLES',
          link: '#',
          current: false,
        },
        {
          name: 'VIDEOS',
          link: '#',
          current: false,
        },
        {
          name: 'FANS',
          link: '#',
          current: false,
        },
        {
          name: 'NEWS',
          link: '#',
          current: false,
        },
        {
          name: 'SHOP',
          link: '#',
          current: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../style/variables';
section {
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
/* parte sinistra del logo */
.image-logo {
  width: 60px;
}
/* parte destra di navigazione */
ul {
  display: flex;
}
li {
  margin-left: 30px;
  position: relative;
}
li {
}
.underline {
  position: absolute;
  height: 5px;
  width: 100%;
  background-color: $main_color;
  left: 0;
  top: 300%;
  display: none;
}
.current + .underline {
  display: block;
}
.current {
  color: $main_color;
}
</style>
