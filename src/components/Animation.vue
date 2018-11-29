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
        'name': 'Mobile Assistant',
        'url': '',
        'tags': ['Animation', 'Sound Effects']
      },{
        'name': 'Mobile Assistant',
        'url': '',
        'tags': ['Animation', 'Sound Effects']
      },{
        'name': 'Building Regulation for Resilience Video | World Bank',
        'url': '',
        'tags': ['Character Animation']
      }]
    }
  }
}
</script>