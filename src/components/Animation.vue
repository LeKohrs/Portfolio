<template>
  <div class="animations">
    <ul>
      <li v-for="(video, key) in videos" :key="key" class="video">
        <a :href="video.url">{{ video.name }}</a>
        <p v-for="(tag, key) in video.tags" :key="key">{{ tag }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Animation',
  data() {
    return {
      videos: [{
        'name': 'Leave the Elephant Behind | Mobile Assistant',
        'url': 'https://youtu.be/f4g94OlEXxo',
        'tags': ['Animation', 'Sound Effects']
      },{
        'name': 'Elephant in the Room | Mobile Assistant',
        'url': 'https://youtu.be/Aapd8ytYS2o',
        'tags': ['Animation', 'Sound Effects']
      },{
        'name': 'Building Regulation for Resilience Video | World Bank',
        'url': 'https://www.youtube.com/watch?v=XMVLEnjzoAI',
        'tags': ['Character Animation']
      }]
    }
  }
}
</script>
<style type="scss">
  
</style>
