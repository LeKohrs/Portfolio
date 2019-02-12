<template>
  <div class="home">
    <Logo />
    <h1>Ryan Leichliter</h1> 
    <Skills :showWeb="showWeb" :showAnimation="showAnimation"/>    
    <div class="toggle">
      <p class="toggle__web" @click="selectWeb">Web Sites</p>  
      <div class="toggle__btn" @click="toggleSkills">
        <div class="icon-container" :class="[{ web: showWeb }, { animation: showAnimation}]">
          <Code />
          <Play />      
        </div>
      </div>
      <p class="toggle__animation" @click="selectAnimation">Animation</p>    
    </div>
    <div class="content">
      <transition name="slide">
        <div v-if="showWeb" class="web-container">
          <Web />    
        </div>
      </transition>
      <transition name="slide">
        <div v-if="showAnimation" class="animation-container">
          <Videos />            
        </div>
      </transition>
    </div>
    <div class="contact">
      <p>Contact Me!</p>
      <div class="contact__info">
        <a href="mailto:ryan.leichliter@icloud.com" class="email">
          <Email />
        </a>
        <a href="https://www.linkedin.com/in/ryan-leichliter-04a73b78/" class="linked-in" target="_blank">
          <Linkedin />
        </a>
      </div>
    </div>
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
import Email from '@/components/svg/Email.vue'
import Linkedin from '@/components/svg/Linkedin.vue'

export default {
  name: 'home',
  data() {
    return {
      showWeb: true,
      showAnimation: false,
      showContact: false,
    }
  },
  components: {
    Web,
    Videos,
    Skills,
    Logo,
    Play,
    Code,
    Email,
    Linkedin
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
    },
    selectWeb() {
      this.showWeb = true
      this.showAnimation = false
    },
    selectAnimation() {
      this.showWeb = false
      this.showAnimation = true
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
    transition: .3s;

    &:hover {
      color: #2c3e50;
    }

    &.link__url {
      color: #2c3e50;
      text-align: center;
      &:hover {
        color: #4580aa;
      }
    }
  }
  p.link__url {
    font-family: 'Gotham-Bold', Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
  }
  .home {
    overflow: hidden;
  }
  .content {
    position: relative;
  }
  .web-container,
  .animation-container {
    width: 80%;
    max-width: 1000px;
    margin: 0 auto;
    margin-top: 40px;
    text-align: left;
  }
  .links {
    ul {  
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      flex-wrap: wrap;
    }
  }
  .description {
    margin: 8px auto;
    max-width: 100%;
    font-size: 13px;
  }
  .toggle {
    display: flex;
    align-items: center;
    flex-wrap: nowrap;
    max-width: 220px;
    margin: 0 auto 15px;

    p {
      font-size: 10px;
    }

    &__animation,
    &__web {
      cursor: pointer;
      transition: .3s;

      &:hover {
        color: #4580aa;
      }
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
      transition: .3s;

      &:hover {
       border: 1px solid #4580aa; 

       & .icon-container {
         border: 1px solid #4580aa;
       }
      }

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
  .contact__info {
    display: flex;
    align-items: center;
    justify-content: center;

    .email {
      &:hover {
        svg {
          .st0 {
            stroke: #2c3e50;
          }
          .st1 {
            fill: #2c3e50;
          }
        }
      }
    }
    .linkedin {
      &:hover {
        svg {
          .st0 {
            fill: #2c3e50;
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
  @media only screen and (max-width: 1200px) {
    .web-container,
    .animation-container {
      width: 80%;
      max-width: 800px;
      margin: 0 auto;
      margin-top: 40px;
      text-align: left;
    }
    .links {
      ul {  
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;

        .link {
          width: 100%;

          a,
          p {
            max-width: 100%;
          }
        }
      }
    }
  }
</style>
