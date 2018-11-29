<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Skills />
    <transition name="slide">
      <div v-if="showWeb" class="web">
        <Links />    
      </div>
    </transition>
    <transition name="slide">
      <div v-if="showAnimation" class="animation">
        <Videos />            
      </div>
    </transition>
  </div>
</template>

<script>
// @ is an alias to /src
import Links from '@/components/Links.vue'
import Videos from '@/components/Animation.vue'
import Skills from  '@/components/Skills.vue'

export default {
  name: 'home',
  components: {
    Links,
    Videos,
    Skills
  }
}
</script>
<style type="scss">
  ul {
    padding: 0;
  }
  li {
    list-style-type: none;
  }
  a {
    text-decoration: none;
  }
  .slide-enter-active {
    transition: all .3s ease;
  }
  .slide-fade-leave-active {
    transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
  }
  .slide-leave-to,
  .slide-enter {
    transform: translateX(10px);
    opacity: 0;
  }
</style>
