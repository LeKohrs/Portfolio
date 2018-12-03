<template>
  <div class="play">
    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 8.9 11.5" style="enable-background:new 0 0 8.9 11.5;" xml:space="preserve">
      <polygon class="st0" points="0,0 0,11.5 8.9,5.7 "/>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'Play'
}
</script>

<style lang="scss">
  .play {
    position: absolute;
    top: 50%;
    left: 59%;
    width: 75%;    
    transform: translate(-50%, -50%);

    svg {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 62%;    
      transform: translate(-50%, -50%);
    }
    .st0 {
      fill:#4580AA;
    }
  }
</style>
