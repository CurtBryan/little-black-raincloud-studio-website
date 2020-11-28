<template>
  <div id="app">
    <div class="nav">
      <NavBar />
    </div>
    <div class="body-footer-wrapper">
      <div class="body">
        <router-view />
      </div>
      <div class="footer">
        <footer>Hey</footer>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "../src/components/NavBar/NavBar";
export default {
  name: "App",
  components: {
    NavBar
  }
};
</script>

<style lang="scss">
// * first section is reset css
html {
  box-sizing: border-box;
  font-size: 16px;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

body,
h1,
h2,
h3,
h4,
h5,
h6,
p,
ol,
ul {
  margin: 0;
  padding: 0;
  font-weight: normal;
}

ol,
ul {
  list-style: none;
}

img {
  max-width: 100%;
  height: auto;
}
// * End of Reset CSS

#app {
  font-family: $font-oswald;
  color: $white;
  background-color: $bg;
  min-height: 100vh;
  min-width: 100vw;
  display: flex;
  flex-direction: column;
}
.nav {
  height: 70px;
  max-height: 70px;
}
.body-footer-wrapper {
  min-height: calc(100vh - 70px);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
// .footer {
//   background-color: salmon;
// }
</style>
