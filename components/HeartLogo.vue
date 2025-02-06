<template>
  <div class="heart-logo__container" :style="style">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="44"
      height="41"
      viewBox="0 0 44 41"
      fill="none"
    >
      <g filter="url(#filter0_d_24_68)">
        <path
          d="M4 10.8211C4 7.05389 7.05389 4 10.8211 4H33.1789C36.9461 4 40 7.05389 40 10.8211V23.7053C40 27.4724 36.9461 30.5263 33.1789 30.5263C33.1789 30.5263 33.1789 30.5263 33.1789 30.5263C33.1789 30.5263 32.6373 30.5263 29.4842 30.5263C26.3312 30.5263 24.7474 36.3526 22 36.3526C19.2526 36.3526 17.6689 30.5263 14.5158 30.5263C11.3627 30.5263 10.8211 30.5263 10.8211 30.5263C10.8211 30.5263 10.8211 30.5263 10.8211 30.5263C7.05389 30.5263 4 27.4724 4 23.7053V10.8211Z"
          fill="#00ACFF"
        />
      </g>
      <path
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M18.2623 14.1051C18.7954 13.4825 19.6394 13.0824 20.5053 13.0356C21.3952 12.9875 22.3115 13.3125 22.938 14.156C23.561 14.9946 23.9698 16.1838 23.4298 17.5939C22.891 19.0008 21.4109 20.6184 18.2806 22.3258L18.2738 22.3135L18.2581 22.3422C15.1278 20.6348 13.6477 19.0172 13.109 17.6103C12.5689 16.2002 12.9777 15.011 13.6007 14.1724C14.2273 13.3289 15.1435 13.0039 16.0334 13.052C16.8917 13.0984 17.7285 13.4919 18.2623 14.1051Z"
        fill="white"
      />
      <path
        d="M30.0571 13.7578V21.3368H28.9099V14.905H28.8655L27.0521 16.0892V14.9938L28.9432 13.7578H30.0571Z"
        fill="white"
      />
      <defs>
        <filter
          id="filter0_d_24_68"
          x="0"
          y="0"
          width="44"
          height="40.3525"
          filterUnits="userSpaceOnUse"
          color-interpolation-filters="sRGB"
        >
          <feFlood flood-opacity="0" result="BackgroundImageFix" />
          <feColorMatrix
            in="SourceAlpha"
            type="matrix"
            values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
            result="hardAlpha"
          />
          <feOffset />
          <feGaussianBlur stdDeviation="2" />
          <feComposite in2="hardAlpha" operator="out" />
          <feColorMatrix
            type="matrix"
            values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.75 0"
          />
          <feBlend
            mode="normal"
            in2="BackgroundImageFix"
            result="effect1_dropShadow_24_68"
          />
          <feBlend
            mode="normal"
            in="SourceGraphic"
            in2="effect1_dropShadow_24_68"
            result="shape"
          />
        </filter>
      </defs>
    </svg>
  </div>
</template>
<script setup>
const screenWidth = 400
const startX = Math.floor(Math.random() * screenWidth) - screenWidth / 2
const startY = Math.floor(Math.random() * -100)
const animationTargetX = startX
const animationTargetY =
  Math.floor(Math.random() * (600 - startY) + Math.abs(startY) * 2) * -1
const duration = Math.random() * 2 + 3
const scale = Math.random() + 1
const delay = Math.random() * 2

const style = `transform: translate(${startX}px, ${startY}px) scale(${scale}); --animationTargetX: ${animationTargetX}px; --animationTargetY: ${animationTargetY}px; --duration: ${duration}s; --scale: ${scale}; --delay: ${delay}s;`
</script>
<style lang="scss" scoped>
.heart-logo {
  &__container {
    animation: bubble var(--duration) linear var(--delay) infinite;
    opacity: 0;
    position: absolute;
  }

  @keyframes bubble {
    0% {
      opacity: 0;
    }
    5% {
      opacity: 100%;
    }
    60% {
      opacity: 100%;
    }
    100% {
      opacity: 0%;
      transform: translate(var(--animationTargetX), var(--animationTargetY))
        scale(0.8);
    }
  }
}
</style>
