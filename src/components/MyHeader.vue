<template>
  <div>
    <div class="container">
      <section>
        <div class="col-sx">
          <div class="image-logo">
            <img src="../assets/img/dc-logo.png" alt="Logo DC Comics" />
          </div>
        </div>
        <div class="col-dx">
          <nav>
            <ul>
              <li v-for="(pippo, index) in sitesection" :key="index">
                <a :class="{ current: pippo.current }" :href="pippo.link">{{
                  pippo.name
                }}</a>
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
.image-logo {
  width: 60px;
}
ul {
  display: flex;
}
li {
  margin-left: 30px;
}
li {
  .current {
    border-bottom: 5px solid $main_color;
  }
}
.current {
  color: $main_color;
}
</style>
