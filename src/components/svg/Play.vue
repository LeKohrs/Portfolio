<template>
  <div class="play">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" x="0px" y="0px"><title>Play</title><g><path d="M33.1,30.89l31.23,20-31.23,20v-40m-3-8.49a3,3,0,0,0-3,3V76.32a3,3,0,0,0,3,3,3,3,0,0,0,1.61-.48l39.8-25.46a3,3,0,0,0,0-5.05L31.72,22.88a3,3,0,0,0-1.61-.48Z"></path></g></svg>
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
    left: 50%;
    width: 80%;    
    transform: translate(-50%, -50%);

    svg {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 100%;    
      transform: translate(-50%, -50%);
    }
  }
</style>
