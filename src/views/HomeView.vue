<template>
  <div class="home">
    <h3>Home View</h3>
  </div>
</template>

<script>
// @ is an alias to /src

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
