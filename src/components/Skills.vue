<template>
  <div class="skills">
    <transition name="slide">
      <ul v-if="showWeb" class="skills--web">
        <li v-for="(skill, key) in skills.web" :key="key" class="skill--web">
          {{ skill }}
        </li>
      </ul>
    </transition>
    <transition name="slide">
      <ul v-if="showAnimation" class="skills--animation">
        <li v-for="(skill, key) in skills.animation" :key="key" class="skill--animation">
          {{ skill }}
        </li>
      </ul>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  props: ['showWeb', 'showAnimation'],
  data() {
    return {
      skills: {
        'web': ['Vue.js', 'Javascript', 'ES6', 'Drupal'],
        'animation': ['After Effects', 'Illustrator', 'Gifs', 'Videos']
      }
    }
  }
}
</script>