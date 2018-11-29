<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Skills />
    <Links />
    <Videos />
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
