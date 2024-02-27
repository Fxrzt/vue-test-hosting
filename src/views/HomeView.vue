<template>
  <div class="home">
    <NavbarMenu></NavbarMenu>
    <div class="grid grid-cols-4 gap-4 py-2">
      <img src="../img/Beagle Puppies.jpg" class="w-20 h-30">
      <img :src="ImageBeaglePuppy" class="w-20 h-30">
      <img :src="ImageBeaglePuppy" class="w-20 h-30">
      <img :src="ImageBeaglePuppy" class="w-20 h-30">
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
      ImageBeaglePuppy: process.env.IMAGE_BEAGLE_PUPPY
    }
  },
  components: {
    NavbarMenu
  }
}
</script>
