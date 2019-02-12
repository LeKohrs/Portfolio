<template>
  <div class="links">
    <ul>
      <li v-for="(link, key) in links" :key="key" class="link">
        <a v-if="link.url" :href="link.url" class="img-link" target="_blank">
          <img v-bind:src="getImage(link.image)"  />
        </a>
        <img v-else class="img-link" v-bind:src="getImage(link.image)"  />
        <a v-if="link.url" class="link__url" :href="link.url" target="_blank">{{ link.name }}</a>
        <p v-else class="link__url">{{ link.name }} </p>
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
        'type': 'website',
        'image': 'textron'
      },{
        'name': 'Cushman.com',
        'description': 'This was a site built at Swanson Russell. I was part of a team and focused on the front end elements using SASS and javascript.',
        'url': 'https://cushman.txtsv.com/',
        'tags': ['Front End', 'Back End', 'Drupal', 'Javascript'],
        'type': 'website',
        'image': 'cushman'
      },{
        'name': 'TRUSimulation.com',
        'description': 'I was part of the rebuild team on this one. Working on both backend and front end elements.',
        'url': 'https://www.trusimulation.com/',
        'tags': ['Front End', 'Back End', 'Drupal', 'Javascript'],
        'type': 'website',
        'image': 'tru'
      },{
        'name': 'Sea of Sameness',
        'description': 'This was a trivia game built for a trade show. It was controlled by the booth operator on their laptop and the game itself was displayed on a separate browser window for the booth visitors to see. The operator browser window would have to communicate the commands to the visitor browser window to control when to start and stop the game. The visitor would spin a wheel at the booth table and a raspberry pi 3 would send the resulting category to the visitor window. The visitor would then have to guess the word before the timer was up. Built at Swanson Russell.',
        'url': '',
        'tags': ['Front End', 'Back End', 'Vue.js', 'Javascript', 'Raspberry Pi'],
        'type': 'website',
        'image': 'sea'
      },
      {
        'name': 'Marriott Micro Sites | Fort Lauderdale',
        'description': 'These were a series of promotional Microsite infographics. Each site was designed to show information in a fun and interesting way and featured complex Greensock animation. Built while part of the Lemonly team. This Fort Lauderdale site is a good example.',
        'url': 'https://fort-lauderdale-cc289.firebaseapp.com/',
        'tags': ['Front End', 'Back End', 'Javascript', 'Greensock'],
        'type': 'website',
        'image': 'marriott'
      },{
        'name': 'Interactive Sites | Simon Says',
        'description': 'I\'ve also been able to build some fun interactive sites that use physical objects in the world to interact with or navigate a website. Simon Says was designed to use fruit to play the game. Each piece of fruit would represent a different color. You would touch the fruit and a raspberry pie 3 would update the game through a database.',
        'url': 'https://simon-says-e5079.firebaseapp.com/#',
        'tags': ['Front End', 'Back End', 'Vue.js', 'Javascript', 'Raspberry Pi'],
        'type': 'website',
        'image': 'SimonSays'
      },{
        'name': 'Lobby Display',
        'description': 'This internal project was created to give a consistent and easily editable slideshow throughout all the displays within the offices of Swanson Russell. Slides were completely editable and could use picture or video backgrounds with many different slide types including client welcome slides and congratulation slides for employees.',
        'url': '',
        'tags': ['Front End', 'Back End', 'Drupal', 'Vue.js', 'Javascript'],
        'type': 'website',
        'image': ''
      }
      ]
    }
  },
  methods: {
    getImage(img) {
      if(img) {
        var image = require.context('../assets/imgs/', false, /\.jpg$/)

        return image('./' + img + ".jpg")
      }
    }
  }
}
</script>

<style lang="scss">
  
  .link {
    width: calc(100% / 2 - 30px);
    margin-bottom: 50px;

    &:last-child {
      margin-bottom: 0;
    }

    &__url {  
      display: block;
    }


    .img-link {
      display: block;
      max-width: 100%;
      margin: 0 auto 20px;
      

      img {
        width: 100%;
        border: 1px solid #dddddd;
      }
    }
    img.img-link {
      // border: 1px solid #dddddd;
    }
  }
  .roles {
    display: flex;
    flex-wrap: nowrap;
    font-size: 11px;
    color: #4580aa;
    margin: 0 auto;
    max-width: 100%;

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
