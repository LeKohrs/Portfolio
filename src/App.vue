<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
@font-face {
    font-family:'Gotham-Book';
    src: url('../src/assets/fonts/Gotham-Book_gdi.eot');
    src: url('../src/assets/fonts/Gotham-Book_gdi.eot?#iefix') format('embedded-opentype'),
    url('../src/assets/fonts/Gotham-Book_gdi.woff') format('woff'),
    url('../src/assets/fonts/Gotham-Book_gdi.ttf') format('truetype'),
    url('../src/assets/fonts/Gotham-Book_gdi.svg#Gotham-Book') format('svg');
    font-weight: 300;
    font-style: normal;
    font-stretch: normal;
    unicode-range: U+0020-2212;
}

@font-face {
    font-family:'Gotham-Medium';
    src: url('../src/assets/fonts/Gotham-Medium_gdi.eot');
    src: url('../src/assets/fonts/Gotham-Medium_gdi.eot?#iefix') format('embedded-opentype'),
    url('../src/assets/fonts/Gotham-Medium_gdi.woff') format('woff'),
    url('../src/assets/fonts/Gotham-Medium_gdi.ttf') format('truetype'),
    url('../src/assets/fonts/Gotham-Medium_gdi.svg#Gotham-Medium') format('svg');
    font-weight: 300;
    font-style: normal;
    font-stretch: normal;
    unicode-range: U+0020-2212;
}

@font-face {
  font-family:'AGaramondPro-Regular';
  src: url('../src/assets/fonts/AGaramondPro-Regular_gdi.eot');
  src: url('../src/assets/fonts/AGaramondPro-Regular_gdi.eot?#iefix') format('embedded-opentype'),
  url('../src/assets/fonts/AGaramondPro-Regular_gdi.woff') format('woff'),
  url('../src/assets/fonts/AGaramondPro-Regular_gdi.ttf') format('truetype'),
  url('../src/assets/fonts/AGaramondPro-Regular_gdi.svg#AGaramondPro-Regular') format('svg');
  font-weight: 400;
  font-style: normal;
  font-stretch: normal;
  unicode-range: U+0020-25CA;
}

@font-face {
  font-family:'MicrobrewOne-Regular';
  src: url('../src/assets/fonts/MicrobrewOne_gdi.eot');
  src: url('../src/assets/fonts/MicrobrewOne_gdi.eot?#iefix') format('embedded-opentype'),
  url('../src/assets/fonts/MicrobrewOne_gdi.woff') format('woff'),
  url('../src/assets/fonts/MicrobrewOne_gdi.ttf') format('truetype'),
  url('../src/assets/fonts/MicrobrewOne_gdi.svg#MicrobrewOne-Regular') format('svg');
  font-weight: 400;
  font-style: normal;
  font-stretch: normal;
  unicode-range: U+0020-25CA;
}

@font-face {
  font-family:'Gotham-Bold';
  src: url('../src/assets/fonts/Gotham-Bold_gdi.eot');
  src: url('../src/assets/fonts/Gotham-Bold_gdi.eot?#iefix') format('embedded-opentype'),
  url('../src/assets/fonts/Gotham-Bold_gdi.woff') format('woff'),
  url('../src/assets/fonts/Gotham-Bold_gdi.ttf') format('truetype'),
  url('../src/assets/fonts/Gotham-Bold_gdi.svg#Gotham-Bold') format('svg');
  font-weight: 400;
  font-style: normal;
  font-stretch: normal;
  unicode-range: U+0020-2212;
}
#app {
  font-family: 'Gotham-Book', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #4580aa;
    }
  }
}
a {
  font-family: 'Gotham-Bold', Helvetica, Arial, sans-serif;
}
</style>
