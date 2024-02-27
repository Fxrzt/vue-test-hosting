<template>
  <div class="home">
    <NavbarMenu></NavbarMenu>
    <div class="grid grid-cols-4 gap-4 py-2">
      <img v-for="(item, index) in url_image" :key="index" :src=item.image_path class="w-20 h-30">
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarMenu from '../components/NavbarMenu.vue'

export default {
  name: 'HomeView',
  data () {
    return {
      // ImageBeaglePuppy: process.env.IMAGE_BEAGLE_PUPPY,
      url_image: [
        {
          image_name: 'beagle puppies1',
          image_path: '../img/Beagle Puppies.jpg'
        },
        {
          image_name: 'beagle puppies2',
          image_path: '../img/Beagle Puppies.jpg'
        },
        {
          image_name: 'beagle puppies3',
          image_path: '../img/Beagle Puppies.jpg'
        },
        {
          image_name: 'beagle puppies4',
          image_path: '../img/Beagle Puppies.jpg'
        }
      ]
    }
  },
  components: {
    NavbarMenu
  }
}
</script>
