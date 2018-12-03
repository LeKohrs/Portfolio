<template>
  <div class="home">
    <Logo />
    <h1>Ryan Leichliter</h1> 
    <Skills :showWeb="showWeb" :showAnimation="showAnimation"/>    
    <div class="toggle">
      <p>Web Sites</p>  
      <div class="toggle__btn" @click="toggleSkills">
        <div class="icon-container" :class="[{ web: showWeb }, { animation: showAnimation}]">
          <Code />
          <Play />      
        </div>
      </div>
      <p>Animation</p>    
    </div>
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
import Play from '@/components/svg/Play.vue'
import Code from '@/components/svg/Code.vue'

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
    Logo,
    Play,
    Code
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
<style lang="scss">
  h1 {
    margin-bottom: 0;
    font-size: 36px;
  }
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
  .toggle {
    display: flex;
    align-items: center;
    flex-wrap: nowrap;
    max-width: 220px;
    margin: 0 auto 15px;
    // transform: translateX(50px);

    p {
      font-size: 10px;
    }

    .toggle__btn {
      display: block;
      position: relative;
      width: 75px;
      height: 30px;
      margin: 0 auto;
      padding: 0 2px;
      border: 1px solid #B2B4B7;
      border-radius: 20px;
      cursor: pointer;

      .icon-container {
        position: relative;
        top: 50%;
        width: 25px;
        height: 25px;
        border: 1px solid #B2B4B7;
        border-radius: 50%;
        transform: translate(0, -50%) rotate(0deg);
        transition: all .5s;

        &.web {
          .code,
          .play {
            transition: .5s;
          }
          .code {
            opacity: 1;
          }
          .play {
            opacity: 0;
          }
        }
        &.animation {
          transform: translate(45px, -50%) rotate(360deg);

          .code {
            opacity: 0;
          }
          .play {
            opacity: 1;
          }
        }
      }
    }
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
