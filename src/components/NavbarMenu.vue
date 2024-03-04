<template>
  <section class="">
    <nav class=" max-w-screen flex items-center justify-between px-4 md:px-4.5 lg:px-6 bg-black ">
      <a href="/" class=" space-x-3 rtl:space-x-reverse">
        <span
          class="sty_logo self-center text-2xl font-semibold whitespace-nowrap text-white"
          >Gavyn Miles</span
        >
      </a>
      <ul
        class="hidden w-auto lg:flex items-center p-4 md:p-0 border rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse mt-0 border-0 "
      >
        <li v-for="(item, index) in menubar" :key="index">
          <a
            v-if="index == 4"
            @click="fn_getName"
            href="/"
            class="topic_text_TH outline_solid py-2.5 block z-1 xl:px-5 md:px-2 text-white rounded md:text-white hover:text-white"
            aria-current="page"
            >{{ item.name }}</a
          >
          <a
            v-else
            @click="fn_getName"
            :href="item.name_path"
            class="topic_text_TH nav_item block z-0 px-2 text-white rounded hover:bg-gray-100 hover:bg-transparent "
            >{{ item.name }}</a
          >
        </li>
      </ul>
      <div class="item_mobile lg:hidden">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="text-white w-6 h-7">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </div>
    </nav>
    <!-- <nav class="nav_moblie lg:hidden flex items-center justify-between bg-black">
      <a href="/" class=" space-x-3 rtl:space-x-reverse">
        <span
          class="sty_logo self-center text-lg font-semibold whitespace-nowrap text-white"
          >Gavyn Miles</span
        >
      </a>
      <div class="item_mobile">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="text-white w-6 h-7">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </div>
    </nav> -->
  </section>
</template>

<script>
export default {
  name: 'MenuNavbar',
  data () {
    return {
      nameGame: 'game',
      toggleMenu: false,
      menubar: [
        {
          name: 'Home',
          name_path: '/'
        },
        {
          name: 'Skills',
          name_path: '/service'
        },
        {
          name: 'Work Experience',
          name_path: '/about'
        },
        {
          name: 'Contact Me',
          name_path: '/calculate'
        },
        {
          name: 'Hire Me',
          name_path: '/valentine'
        }
      ]
    }
  },
  methods: {
    fn_getName () {
      return console.log(`${this.nameGame}`)
    }
  }
}
</script>

<style scoped>
.sty_logo{
  font-family: 'Lemon', serif;
  /* font-family: 'K2D', sans-serif; */
  font-size: 1.7rem;
  font-weight: 500;
}
.sty_logo:hover{
  background: -webkit-repeating-linear-gradient(#a993fe, #7e61e7);
  /* #f97316 #a993fe #7e61e7 */
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.topic_text_TH {
  font-weight: 500;
  font-size: 1.15rem;
  font-family: 'K2D', sans-serif;
}
.outline_solid{
  background: -webkit-linear-gradient(#a993fe -0.13%, #7e61e7 99.87%);
}
.outline_solid:hover{
  outline: 2px solid #7e61e7;
  background: transparent;
}
.nav_item{
  cursor: pointer;
  position: relative;
  text-decoration: none;
}
.nav_item::before {
  content: " ";
  width: 2rem;
  height: 0.2rem;
  background: linear-gradient(90deg, #a993fe 0%, #7e61e7 100%);
  border-radius: 0.5rem;
  position: absolute;
  bottom: -0.6rem;
  opacity: 0;
  transform: translateX(-1.5rem);
  transition: all 0.3s ease;
}
.nav_item:hover::before{
  width: 100%;
  transform: translateX(-0.25rem);
  opacity: 1;
}
</style>
