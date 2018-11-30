<template>
  <div class="home">
    <Logo />
    <div class="toggle__btn" @click="toggleSkills"></div>
    <Skills :showWeb="showWeb" :showAnimation="showAnimation"/>
    <transition name="slide">
      <div v-if="showWeb" class="web">
        <Web />    
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
import Web from '@/components/Web.vue'
import Videos from '@/components/Animation.vue'
import Skills from  '@/components/Skills.vue'
import Logo from  '@/components/svg/Logo.vue'

export default {
  name: 'home',
  data() {
    return {
      showWeb: true,
      showAnimation: false
    }
  },
  components: {
    Web,
    Videos,
    Skills,
    Logo
  },
  methods: {
    toggleSkills() {
      if(this.showWeb) {
        this.showWeb = false
        this.showAnimation = true
      }
      else {
        this.showWeb = true
        this.showAnimation = false
      }
    }
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
    color: #4580aa;
  }
  .home {
    overflow: hidden;
  }
  .toggle__btn {
    display: block;
    position: relative;
    width: 75px;
    height: 30px;
    margin: 0 auto;
    border: 2px solid #222;
    border-radius: 20px;
    cursor: pointer;
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
