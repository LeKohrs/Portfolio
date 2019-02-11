<template>
  <div class="links">
    <ul>
      <li v-for="(link, key) in links" :key="key" class="link">
        <a v-if="link.url" class="link__url" :href="link.url" target="_blank">{{ link.name }}</a>
        <p v-else class="link__url">{{ link.name }}
        <p class="description"> {{ link.description }}</p>
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
        'description': 'Microsite built at Swanson Russell to introduce Textron Off Roads newest vehicle. I was able to use a number of different skills on this site. Most notable would be the canvas dirt specs in the marquee and the 360 spinner.',
        'url': 'https://rideovereverything.com/',
        'tags': ['Front End', 'Back End', 'Canvas', '360 Player'],
        'type': 'website'
      },{
        'name': 'Cushman.com',
        'description': 'This was a site built at Swanson Russell. I was part of a team and focused on the frontend elements using SASS and javascript.',
        'url': 'https://cushman.txtsv.com/',
        'tags': ['Front End', 'Back End', 'Drupal', 'Javascript'],
        'type': 'website'
      },{
        'name': 'TRUSimulation.com',
        'description': 'I was part of the rebuild team on this one. Working on both backend and frontend elements.',
        'url': 'https://www.trusimulation.com/',
        'tags': ['Front End', 'Back End', 'Drupal', 'Javascript'],
        'type': 'website'
      },{
        'name': 'Lobby Display',
        'description': 'This internal project was created to give a consistent and easily editable slideshow throughout all the displays within the offices of Swanson Russell. Slides were completely editable and could use picture or video backgrounds with many different slide types including client welcome slides and congratulation slides for employees.',
        'url': '',
        'tags': ['Front End', 'Back End', 'Drupal', 'Vue.js', 'Javascript'],
        'type': 'website'
      },{
        'name': 'Sea of Sameness',
        'description': 'This was a trivia game built for a trade show. It was controlled by the booth operator on their laptop and the game itself was displayed on a separate browser window for the booth visitors to see. The operator browser window would have to communicate the commands to the visitor browser window to control when to start and stop the game. The visitor would spin a wheel at the booth table and a raspberry pi 3 would send the resulting category to the visitor window. The visitor would then have to guess the word before the timer was up. Built at Swanson Russell.',
        'url': '',
        'tags': ['Front End', 'Back End', 'Vue.js', 'Javascript', 'Raspberry Pi'],
        'type': 'website'
      },
      {
        'name': 'Marriott Micro Sites',
        'description': 'These were a series of promotional Microsite infographics. Each site was designed to show information in a fun and interesting way and featured complex Greensock animation. Built while part of the Lemonly team.',
        'url': '',
        'tags': ['Front End', 'Back End', 'Javascript', 'Greensock'],
        'type': 'website'
      }
      ]
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
    font-size: 11px;
    color: #4580aa;

    p {
      position: relative;
      margin-top: 0;
      margin-right: 15px;
      font-weight: 700;  

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
