<template>
  <div id="app">
    <div class="wrapper">
      <div id="navbar-small" role="navigation" v-bind:class="{ open: !isOpen }" v-on:click="isOpen = !isOpen">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>
      <div class="menu-wrapper" v-bind:class="{ open: !isOpen }">
        <Menu v-on:toggleMenu="toggleMenu" />
      </div>
      <div class="content-container">
        <router-view />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
/* http://meyerweb.com/eric/tools/css/reset/
   v4.0 | 20180602
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
main, menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, main, menu, nav, section {
  display: block;
}
/* HTML5 hidden-attribute fix for newer browsers */
*[hidden] {
  display: none;
}
body {
  line-height: 1;
}
ol, ul {
  list-style: none;
}
blockquote, q {
  quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}

/* Roboto Light */
@font-face {
  font-family: 'Montserrat';
  src: url("./assets/fonts/Montserrat-Light.ttf") format("truetype");
  font-weight: 300;
  font-style: normal;
}
@font-face{
    font-family: 'ftnk';
    src:url(https://use.typekit.net/af/9b05f3/000000000000000000013365/27/l?subset_id=2&fvd=n4&v=3) format("woff2"),
    url(https://use.typekit.net/af/9b05f3/000000000000000000013365/27/d?subset_id=2&fvd=n4&v=3) format("woff"),
    url(https://use.typekit.net/af/9b05f3/000000000000000000013365/27/a?subset_id=2&fvd=n4&v=3) format("opentype");
    font-weight:400;
    font-style:normal;
}
@font-face{
    font-family: 'ftnk';
    src:url(https://use.typekit.net/af/309dfe/000000000000000000010091/27/l?subset_id=2&fvd=n7&v=3) format("woff2"),
    url(https://use.typekit.net/af/309dfe/000000000000000000010091/27/d?subset_id=2&fvd=n7&v=3) format("woff"),
    url(https://use.typekit.net/af/309dfe/000000000000000000010091/27/a?subset_id=2&fvd=n7&v=3) format("opentype");
    font-weight:700;font-style:normal;}

html {
  font-family: 'Montserrat', Arial, sans-serif;
}

#app {
  // font-family: Avenir, Helvetica, Arial, sans-serif;
  // -webkit-font-smoothing: antialiased;
  // -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
}

.menu-wrapper {
  width: 250px;
  height: 100%;
  position: fixed;
  left: 0;
  top: 0;
  padding: 0 2rem;
  box-sizing: border-box;
  border-right: 1px solid rgba( 0, 0, 0, 0.08 );
  background: #fcfcfc;
  // box-shadow: 1px 1px 2px 1px rgba(0, 0, 0, 0.1);
  // box-shadow: 0px 0px 0px 1px rgba(109, 81, 81, 0.1);
}

.content-container {
  width: calc( 100% - 250px);
  height: 100%;
  padding-left: 250px;
}

#navbar-small {
  position: absolute;
  top: 20px;
  left: 12px;
  transform: rotate(0deg);
  transition: .5s ease-in-out;
  cursor: pointer;
  width: 35px;
  height: 20px;
  z-index: 99;
  display: none;

  span {
    display: block;
    position: absolute;
    height: 3px;
    width: 80%;
    background: #2c3e50;
    border-radius: 9px;
    opacity: 1;
    left: 0;
    transform: rotate(0deg);
    transition: .25s ease-in-out;

    &:nth-child(1) {
      top: 0px;
    }
    &:nth-child(2), &:nth-child(3) {
      top: 8px;
    }
    &:nth-child(4) {
      top: 16px;
    }
  }
}

#navbar-small.open {
  span:nth-child(1) {
    top: 8px;
    width: 0%;
    left: 50%;
  }

  span:nth-child(2) {
    transform: rotate(45deg);
  }

  span:nth-child(3) {
    transform: rotate(-45deg);
  }

  span:nth-child(4) {
    top: 8px;
    width: 0%;
    left: 50%;
  }
}

/* Small (sm) */
@media (max-width: 640px) {
  #navbar-small {
    display: block;
  }

  .menu-wrapper {
    display: none;
    width: 100%;
    // top: 50px;
    z-index: 2;
    padding-top: 3rem;

    &.open {
      display: block;
    }
  }
  .content-container {
    width: 100%;
    padding: 3rem 0 0 0;
    z-index: 1;
  }
}
</style>

<script>
// @ is an alias to /src
import Menu from '@/components/Menu.vue'

export default {
  name: 'Home',
  components: {
    Menu
  },
  data () {
    return {
      isOpen: false
    }
  },
  methods: {
    toggleMenu () {
      // console.log('MenuIsOpen:', MenuIsOpen)
      this.isOpen = true
    }
  }
}
</script>
