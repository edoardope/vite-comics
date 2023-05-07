<script>
import MainContent from "./components/MainContent.vue"
import JumboTron from "./components/JumboTron.vue"

export default {
  name: "App",
  components: {
    JumboTron,
    MainContent,
  },
  data() {
    return {
      a: true,
      sections: [
        {
          iconName: 'DIGITAL COMICS',
          iconUrl: 'buy-comics-digital-comics.png'
        },
        {
          iconName: 'DC MERCHANDISE',
          iconUrl: 'buy-comics-merchandise.png'
        },
        {
          iconName: 'SUBSCRIPTION',
          iconUrl: 'buy-comics-subscriptions.png'
        },
        {
          iconName: 'COMIC SHOP LOCATOR',
          iconUrl: 'buy-comics-shop-locator.png'
        },
        {
          iconName: 'DC POWER VISA',
          iconUrl: 'buy-dc-power-visa.svg'
        },
      ]
    }
  },
  methods: {
    getImagePath: function (imgPath) {
      return new URL(imgPath, import.meta.url).href;
    }
  }
}
</script>

<template>
  <header>
    <img src="./assets/dc-logo.png" alt="">
    <ul>
      <li><a href="">CHARACTERS</a></li>
      <li><a href="">COMICS</a></li>
      <li><a href="">MOVIES</a></li>
      <li><a href="">TV</a></li>
      <li><a href="">GAMES</a></li>
      <li><a href="">COLLECTIBLES</a></li>
      <li><a href="">VIDEO</a></li>
      <li><a href="">FANS</a></li>
      <li><a href="">NEWS</a></li>
      <li><a href="">SHOP</a></li>
    </ul>
  </header>
  <JumboTron />
  <MainContent v-if="a" />
  <section id="a">
    <span v-for="(  element, index  ) in      sections     " :key="index">
      <img :src="getImagePath(`./assets/${element.iconUrl}`)" :alt="element.iconName">
      <span>{{ element.iconName }}</span>
    </span>
  </section>
  <footer>
    <section id="b">
      <div id="footerLink">
        <span>
          <h3>DC COMICS</h3>
          <ul>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
          </ul>
          <h3>DC COMICS</h3>
          <ul>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
          </ul>
        </span>
        <span class="footerColumn">
          <h3>DC COMICS</h3>
          <ul>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
          </ul>
        </span>
        <span class="footerColumn">
          <h3>DC COMICS</h3>
          <ul>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
            <li><a href="">link</a></li>
          </ul>
        </span>
      </div>
      <div id="footerLogo">

      </div>
    </section>
    <section id="c">
      <div>
        <span id="d">
          <a href="">SING-UP NOW!</a>
        </span>
      </div>
      <div>
        <h2>FOLLOW US</h2>
        <img src="./assets/footer-facebook.png" alt="">
        <img src="./assets/footer-twitter.png" alt="">
        <img src="./assets/footer-youtube.png" alt="">
        <img src="./assets/footer-pinterest.png" alt="">
        <img src="./assets/footer-periscope.png" alt="">
      </div>
    </section>
  </footer>
</template>

<style lang="scss">
@use 'style/main.scss' as *;
</style>
