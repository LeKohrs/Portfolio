<template>
  <div class="links">
    <ul>
      <li v-for="(link, key) in links" :key="key" class="link">
        <a class="link__url" :href="link.url" target="_blank">{{ link.name }}</a>
        <div class="roles">
          <p v-for="(tag, key) in link.tags" :key="key">{{ tag }}</p>  
        </div>
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
        'name': 'Ride Over Everything | Textron Off Road',
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

<style lang="scss">
  .link {
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
