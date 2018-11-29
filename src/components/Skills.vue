<template>
  <div class="skills">
    <ul class="skills--web">
      <li v-for="(skill, key) in skills.web" :key="key" class="skill--web">
        {{ skill }}
      </li>
    </ul>
    <ul class="skills--animation">
      <li v-for="(skill, key) in skills.animation" :key="key" class="skill--animation">
        {{ skill }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Skills',
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