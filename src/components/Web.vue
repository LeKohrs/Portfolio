<template>
  <div class="links">
    <ul>
      <li v-for="(link, key) in links" :key="key" class="link">
        <a :href="link.url">{{ link.name }}</a>
        <p v-for="(tag, key) in link.tags" :key="key">{{ tag }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Links',
  data() {
    return {
      msg: 'hello there',
      links: [{
        'name': 'Ride Over Everything',
        'url': 'https://rideovereverything.com/',
        'tags': ['Front End', 'Back End'],
        'type': 'website'
      },{
        'name': 'EZGO',
        'url': 'https://ezgo.txtsv.com',
        'tags': ['Front End', 'Back End'],
        'type': 'website'
      }]
    }
  }
}
</script>