<template>
  <div class="animations">
    <ul>
      <li v-for="(video, key) in videos" :key="key" class="video">
        <a class="video__url" :href="video.url">{{ video.name }}</a>
        <div class="roles">
          <p v-for="(tag, key) in video.tags" :key="key">{{ tag }}</p>        
        </div>
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
<style lang="scss">
  .video {
    margin-bottom: 15px;

    &:last-child {
      margin-bottom: 0;
    }

    &__url {  
      display: block;
    }
  }
  .roles {
    display: inline-flex;
    flex-wrap: nowrap;
    font-size: 12px;

    p {
      position: relative;
      margin-top: 0;
      margin-right: 15px;  

      &:after {
        content: '-';
        position: absolute;
        top: 50%;
        right: -10px;
        opacity: .6;
        transform: translateY(-50%);
      }  
      &:last-child {
        margin-right: 0;

        &:after {
          content: none;
        }
      }
    }
  }
</style>
