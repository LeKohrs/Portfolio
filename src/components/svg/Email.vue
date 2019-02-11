<template>
  <div class="email">  
    <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
        viewBox="0 0 33.5 25.4" style="enable-background:new 0 0 33.5 25.4;" xml:space="preserve">
    <path id="email_1_" class="st0" d="M31.3,23.1L21.5,13 M2.2,23.2l10.1-10.3 M1.7,1.7l13.3,13.4c1,1,2.8,1,3.7,0L32,1.8 M32.2,1.4
        L1.4,1.4l0,22.6L32.1,24l0-22.6L32.2,1.4z"/>
    <rect x="31.9" class="st1" width="1.6" height="1.7"/>
    </svg>
  </div>
</template>
<script>
export default {
  name: 'Email'
}
</script>
<style lang="scss">
  .email{
    width: 35px;

    svg {
        width: 100%;

        .st0{
          fill: none;
          stroke: #4580aa;
          stroke-width: 2.871;
          stroke-miterlimit: 10;
          transition: .3s;
        }
        .st1{
          fill: #4580aa;
          transition: .3s;
        }
    }
    path.line {
      fill: #4580aa;
    }
  }
</style>
