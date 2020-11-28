<template>
  <div class="navbar">
    <div class="logo-wrapper" @click="routerPush('Home')">
      <img alt="Vue logo" src="../../assets/logo.png" />
      <h3>Little Black Raincloud Studio</h3>
    </div>
    <div class="routes-wrapper">
      <div
        @click="routerPush('Home')"
        :class="{ 'active-route': this.$route.name === 'Home' }"
      >
        <p>Home</p>
      </div>
      <div
        @click="routerPush('About')"
        :class="{ 'active-route': this.$route.name === 'About' }"
      >
        <p>About</p>
      </div>
      <div
        @click="routerPush('Music')"
        :class="{ 'active-route': this.$route.name === 'Music' }"
      >
        <p>Music</p>
      </div>
      <div
        @click="routerPush('Contact')"
        :class="{ 'active-route': this.$route.name === 'Contact' }"
      >
        <p>Contact</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  methods: {
    routerPush(routeName) {
      if (this.$route.name.toLowerCase() === routeName.toLowerCase()) return;
      return this.$router.push({ name: `${routeName}` });
    }
  }
};
</script>

<style lang="scss" scoped>
.navbar {
  background-color: $gray;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
  padding: 0 50px;
}
.logo-wrapper {
  height: 100%;
  display: flex;
  align-items: center;
  color: $black;
  font-family: $font-bebas;
  font-size: $font-xlarge;
  cursor: pointer;
  &:hover {
    border-bottom: 5px solid $green;
    margin-top: 5px;
  }
  img {
    max-height: 100%;
  }
}
.routes-wrapper {
  display: flex;
  height: 100%;
  div {
    display: flex;
    align-items: center;
    text-align: center;
    padding: 10px;
    color: $black;
    cursor: pointer;
    &:hover {
      border-bottom: 5px solid $green;
      p {
        margin-top: 5px;
      }
    }
  }
}
.active-route {
  border-bottom: 5px solid $green;
  p {
    margin-top: 5px;
  }
}
</style>
