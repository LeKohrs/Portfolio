<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Links />
  </div>
</template>

<script>
// @ is an alias to /src
import Links from '@/components/Links.vue'

export default {
  name: 'home',
  components: {
    Links
  }
}
</script>
