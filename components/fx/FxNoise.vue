<script setup lang="ts">

</script>


<template>
  <div class="noise"></div>
</template>

<style lang="scss" scoped>
.noise {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  pointer-events: none;
  z-index: 300;
  transform: translateZ(0);
  overflow: hidden;

  &:before {
    content: "";
    top: -10rem;
    left: -10rem;
    width: calc(100% + 20rem);
    height: calc(100% + 20rem);
    z-index: 9999;
    position: fixed;
    background-image: url('/assets/png/noise.png');
    opacity: 0.15;
    pointer-events: none;
    -webkit-animation: noise 1s steps(2) infinite;
    animation: noise 1s steps(2) infinite;
    overflow: hidden;
  }

  @-webkit-keyframes noise {
    to {
      transform: translate3d(-7rem, 0, 0)
    }
  }

  @keyframes noise {
    0% {
      transform: translate3d(0, 9rem, 0)
    }

    10% {
      transform: translate3d(-1rem, -4rem, 0)
    }

    20% {
      transform: translate3d(-8rem, 2rem, 0)
    }

    30% {
      transform: translate3d(9rem, -9rem, 0)
    }

    40% {
      transform: translate3d(-2rem, 7rem, 0)
    }

    50% {
      transform: translate3d(-9rem, -4rem, 0)
    }

    60% {
      transform: translate3d(2rem, 6rem, 0)
    }

    70% {
      transform: translate3d(7rem, -8rem, 0)
    }

    80% {
      transform: translate3d(-9rem, 1rem, 0)
    }

    90% {
      transform: translate3d(6rem, -5rem, 0)
    }

    to {
      transform: translate3d(-7rem, 0, 0)
    }
  }
}
</style>