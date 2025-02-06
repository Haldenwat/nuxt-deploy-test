<template>
  <div>
    <div class="hero-img__evil-larry">
      <img src="~/assets/evil-larry-larry.png">
    </div>
    <div class="homepage__heart-container">
      <HeartLogo v-for="i in 15"></HeartLogo>
    </div>
    <NuxtRouteAnnouncer />
    <NuxtWelcome />
  </div>
</template>
<script setup>
import HeartLogo from '@/components/HeartLogo.vue'
</script>

<style lang="scss" scoped>
.hero-img {
  &__evil-larry {
      width: 100%;
      display: flex;
      justify-content: center;
      animation: 3s infinite blur;
  }
}

.homepage {
  &__heart-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

@keyframes blur {
  0% {filter: blur(10px);}
  60% {filter: blur(0px);}
}
</style>