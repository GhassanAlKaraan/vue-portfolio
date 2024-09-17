<script setup>
import NavBar from "@/components/NavBar.vue";
import HomeView from "@/views/HomeView.vue";
</script>

<template>
<div class="wrapper">
  <div class="background">
    <div class="spotlights">
      <div class="spotlight-left"><img src="./assets/images/about/spotlight-left.png" alt="spotlight"></div>
      <div class="spotlight-right"><img src="./assets/images/about/spotlight-right.png" alt="spotlight"></div>
    </div>
    </div>
  <div class="foreground">
    <NavBar />
    <HomeView />
  </div>
</div>
</template>

<style scoped>
.background {
  width: 100%;
  position: absolute;
  z-index: 1;
}
.foreground {
  width: 100%;
  position: relative;
  z-index: 5;
}
.spotlights {
  width: 100%;
  display: flex;
  justify-content: space-between;
}
.spotlight-left,
.spotlight-right {
  width: 50%;
}
.spotlight-left img,
.spotlight-right img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

</style>
