<template>
  <div class="code">  
    <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
      viewBox="0 0 18.2 9" style="enable-background:new 0 0 18.2 9;" xml:space="preserve">
    <polygon class="st0" points="6.2,9 7.6,9 12.3,0 10.9,0 "/>
    <polygon class="st1" points="13.1,8.3 18.1,5 18.1,4 13.1,0.7 13.1,1.8 17.2,4.5 13.1,7.2 "/>
    <polygon class="st1" points="5.1,0.7 0.1,4 0.1,5 5.1,8.3 5.1,7.2 1,4.5 5.1,1.8 "/>
    </svg>
  </div>
</template>
<script>
export default {
  name: 'Code'
}
</script>
<style lang="scss">
  .code {
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

      .st0{fill:#4580A9;}
      .st1{fill:#888B90;stroke:#888B90;stroke-width:0.25;stroke-miterlimit:10;}
    }
    path.line {
      fill: #4580aa;
    }
  }
</style>
