<template>
  <div id="js-spinner" class="spinner">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<style scoped lang="scss">
/* Source: https://loading.io/css/ */
.spinner {
  display: flex;
  height: 64px;
  justify-content: center;
  position: absolute;
  opacity: 1;
  transition: 1s opacity;
  width: 100%;

  & div {
    animation: spinner 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
    border: 6px solid $silver;
    border-color: $silver transparent transparent transparent;
    border-radius: 50%;
    box-sizing: border-box;
    display: block;
    height: 51px;
    margin: 6px;
    position: absolute;
    width: 51px;

    &:nth-child(1) {
      animation-delay: -0.45s;
    }

    &:nth-child(2) {
      animation-delay: -0.3s;
    }

    &:nth-child(3) {
      animation-delay: -0.15s;
    }
  }
}

@keyframes spinner {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
