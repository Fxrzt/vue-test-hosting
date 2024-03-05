<template>
  <section>
    <nav class=" max-w-screen flex items-center justify-between p-4 md:px-4.5 lg:px-6 bg-black ">
      <a href="/" class=" space-x-3 rtl:space-x-reverse">
        <span
          class="sty_logo self-center text-2xl font-semibold whitespace-nowrap text-white"
          >Gavyn Miles</span
        >
      </a>
      <ul class="hidden w-auto lg:flex items-center p-4 md:p-0 border rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse mt-0 border-0 ">
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
      <div class="item_mobile lg:hidden cursor-pointer" @click="isActive=!isActive">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="text-white md:w-9 md:h-9 lg:w-8 lg:h-8 w-8 h-8">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </div>
    </nav>
    <div :class="isActive ? 'active_sidebar' : 'non_active'" class="lg:hidden grid grid-rows-4 grid-flow-col gap-4 side_bar bg-black">
      <ul class="w-full lg:flex items-center p-4 md:p-0 border md:flex-row md:space-x-8 border-0 ">
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
    </div>
    <nav class="bg-white border-gray-200 dark:bg-gray-900">
      <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
        <a href="https://flowbite.com/" class="flex items-center space-x-3 rtl:space-x-reverse">
            <img src="https://flowbite.com/docs/images/logo.svg" class="h-8" alt="Flowbite Logo" />
            <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">Flowbite</span>
        </a>
        <button data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false">
            <span class="sr-only">Open main menu</span>
            <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
            </svg>
        </button>
        <div class="hidden w-full md:block md:w-auto" id="navbar-default">
          <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
            <li>
              <a href="#" class="block py-2 px-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white md:dark:text-blue-500" aria-current="page">Home</a>
            </li>
            <li>
              <a href="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">About</a>
            </li>
            <li>
              <a href="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Services</a>
            </li>
            <li>
              <a href="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Pricing</a>
            </li>
            <li>
              <a href="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
export default {
  name: 'MenuNavbar',
  data () {
    return {
      nameGame: 'game',
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
  font-size: 1.7rem;
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
