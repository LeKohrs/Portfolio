<template>
  <div class="logo">
    <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 219.9 219.9" style="enable-background:new 0 0 219.9 219.9;" xml:space="preserve">
      <g id="circle">
        <circle class="st0" cx="110" cy="110" r="103.9"/>
      </g>
      <g id="mainFace">
        <ellipse id="eyeLeft" class="st1" cx="88.7" cy="112.6" rx="3.3" ry="4.3"/>
        <ellipse id="eyeRight" class="st1" cx="130" cy="113.6" rx="3.3" ry="4.3"/>
        <path id="mouth" class="st2" d="M94.7,157.6c0,0,14.3,6.7,26,0.7"/>
        <polyline class="st3" points="108.7,126.9 110,144.2 103.3,143.6 	"/>
        <path id="beard" class="st4" d="M56.9,107.1c0,0-1.1,76.6,44.3,76.6c0,0,1.4-1.2,4-15.4h5.7l1.7,15.4c0,0,40.4,0.7,46.1-57.5
          l1.8,0.7c0,0,0,58.2-53.9,72.3C106.6,199.3,47,199.3,56.9,107.1"/>
        <path id="hair" class="st4" d="M157,73.8c0,0-1.4,21.3,2.8,35.5l-1.9,23.4l7.1-21.3c0,0,9.9-27-7.1-62.1c0,0-37.4-39.4-87.9-4.6
          c0,0-18.8,21.3-18.4,44l1.4,22.7l4.8,17.7l3.8-29.1c0,0,21.8-12.1,18.9-20.6c-2.8-8.5,29.3,4.3,29.3-3.5
          C109.7,75.9,157,51.1,157,73.8"/>
        <path id="glasses" class="st5" d="M63.7,102.8c0,0,2.5,14.2,3.5,17.7c1.1,3.5,31.2,2.8,32.6,1.4c1.4-1.4,5.7-14.2,5.7-14.2h8.5
          l4.3,13.5c0,0,21.1,5.9,34.7,0.8l2.5-18.4c0,0-5.3-6.4-39.4,1.4c-5.9,1.4-9.9,1.4-9.9,1.4S86.1,94.3,63.7,102.8z"/>
      </g>
    </svg>
  </div>
</template>
<script>
export default {
  name: 'Logo'
}
</script>

<style lang="scss">
  
  .logo {
    max-width: 80px;
    margin: 20px auto;

    .st0{fill:none;stroke:#B2B2B2;stroke-width:11.1604;}
    .st1{opacity:0;fill:#231F20;}
    .st2{opacity:0;fill:none;stroke:#231F20;stroke-width:2.7946;stroke-linecap:round;stroke-miterlimit:10;}
    .st3{opacity:0;fill:none;stroke:#231F20;stroke-width:2;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;}
    .st4{fill:#231F20;}
    .st5{fill:none;stroke:#231F20;stroke-width:3.9405;}
  }
</style>
