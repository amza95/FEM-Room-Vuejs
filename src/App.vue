<template>
  <div id="app">
    <div id="nav">
      <div class="nav-bar">
        <div class="title-name">room</div>
        <router-link to="/" class="nav-hover">Home</router-link>
        <router-link to="/shop" class="nav-hover">Shop</router-link>
        <router-link to="/about" class="nav-hover">About</router-link>
        <router-link to="/contact" class="nav-hover">Contact</router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  name: "nav-link-line",
  data() {
    return {
      isHover: false,
    };
  },
};
</script>

<style scoped>
.nav-hover::after {
  opacity: 0;
  position: absolute;
  content: "";
  left: calc(50% - 25%);
  top: 2vw;
  padding: 0;
  margin: 0;
  background: white;
  border-radius: 20px;
  width: 50%;
  height: 0.2vw;
  transition: 1s ease;
}

.nav-hover:hover:after {
  opacity: 1;
  transition: 0.2s ease;
}
</style>
