<template>
  <div class="home">
    <NavbarMenu></NavbarMenu>
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
      ]
    }
  },
  components: {
    NavbarMenu
  },
  methods: {
    fn_getConsoleLog () {
      this.url_image.forEach(data => {
        console.log(data.image_name, data.image_path)
      })
    }
  }
}
</script>
