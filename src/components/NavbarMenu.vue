<template>
  <header>
    <nav class="flex justify-between w-full items-center px-5 py-8">
      <div class="">
        <a href="/" class=" space-x-3 rtl:space-x-reverse">
          <span class="sty_logo self-center font-semibold text-black">
            Gavyn Miles
          </span>
        </a>
      </div>
      <div class="hidden lg:block md:static absolute bg-white md:min-h-fit left-0 top-[-100%] lg:w-auto w-full flex items-center px-5">
        <ul class="topic_text_TH flex md:flex-row flex-col md:items-center md:gap-[4vw] gap-8">
          <li v-for="(item, index) in menubar" :key="index">
            {{ item.name }}
          </li>
        </ul>
      </div>
      <div class="lg:hidden hambarger_bar flex justify-end" @click="isActive=!isActive">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8 text-black">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </div>
    </nav>
    <nav class="grid grid-cols-2 px-4 py-5 items-center" style="border: 2px solid blue;">
      <div>
        <a href="/" class=" space-x-3 rtl:space-x-reverse">
          <span class="sty_logo self-center font-semibold text-black">
            Gavyn Miles
          </span>
        </a>
      </div>
      <div class="hidden">
        <ul>
          <li v-for="(item,index) in menubar" :key="index">
            {{ item.name }}
          </li>
        </ul>
      </div>
      <div class="lg:hidden hambarger_bar" @click="isActive=!isActive">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8 text-black">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'MenuNavbar',
  data () {
    return {
      nameGame: 'You were Clicked',
      isActive: false,
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
@media (min-width: 1024px) {
  .sty_logo:hover{
    background: -webkit-repeating-linear-gradient(#a993fe, #7e61e7);
    /* #f97316 #a993fe #7e61e7 */
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .outline_solid:hover{
    outline: 2px solid #7e61e7;
    background: transparent;
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
  .outline_solid{
    background: -webkit-linear-gradient(#a993fe -0.13%, #7e61e7 99.87%);
  }
}
.sty_logo{
  font-family: 'Lemon', serif;
  /* font-family: 'K2D', sans-serif; */
  font-size: 1.5rem;
  font-weight: 500;
}
.topic_text_TH {
  font-weight: 500;
  font-size: 1.15rem;
  font-family: 'K2D', sans-serif;
}
.nav_item{
  cursor: pointer;
  position: relative;
  text-decoration: none;
}
.side_bar{
  left: 0%;
}
.non_active{
  position: absolute;
  left: -45%;
  height: 100vh;
}
.active_sidebar{
  position: absolute;
  left: 0%;
  width: 85%;
  height: 100vh;
}
</style>
