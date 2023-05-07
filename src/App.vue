<script>
import MainContent from "./components/MainContent.vue"

export default {
  name: "App",
  components: {
    MainContent,
  },
  data() {
    return {
      sections: [
        {
          iconName: 'DIGITAL COMICS',
          iconUrl: './assets/img/buy-comics-digital-comics.png'
        },
        {
          iconName: 'DC MERCHANDISE',
          iconUrl: './assets/img/buy-comics-merchandise.png'
        },
        {
          iconName: 'SUBSCRIPTION',
          iconUrl: './assets/img/buy-comics-subscription.png'
        },
        {
          iconName: 'COMIC SHOP LOCATOR',
          iconUrl: './assets/img/buy-comics-shop-locator.png'
        },
        {
          iconName: 'DC POWER VISA',
          iconUrl: './assets/img/buy-dc-power-visa.png'
        },
      ]
    }
  },
  methods: {

  }
}
</script>

<template>
  <header>
    <img src="./assets/img/dc-logo.png" alt="">
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
  <MainContent />
  <section id="a">
    <span v-for="(element, index) in sections" :key="index">
      <img src="./assets/img/buy-comics-digital-comics.png" :alt="element.iconName">
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
        <span id="e"><i class="fa-brands fa-facebook-f"></i></span>
        <span id="e"><i class="fa-brands fa-twitter"></i></span>
        <span id="e"><i class="fa-brands fa-youtube"></i></span>
        <span id="e"><i class="fa-brands fa-pinterest"></i></span>
        <span id="e"><i class="fa-solid fa-location-dot"></i></span>
      </div>
    </section>
  </footer>
</template>

<style lang="scss">
@use 'style/main.scss' as *;
</style>
