<template>
  <nav class="py-5 px-2 bg-black">
    <div
      class="max-w-screen flex flex-wrap items-center justify-between pl-12 pr-12"
    >
      <a href="#" class="flex items-center space-x-3 rtl:space-x-reverse">
        <span
          class="sty_logo self-center text-2xl font-semibold whitespace-nowrap text-white"
          >Gavyn Miles</span
        >
      </a>
      <div class="hidden w-full md:block md:w-auto">
        <ul
          class=" flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse mt-0 border-0  "
        >
          <li v-for="(item, index) in menubar" :key="index">
            <a
              v-if="index == 4"
              @click="fn_getName"
              href="/"
              class="topic_text_TH block z-1 py-1.5 px-4 text-white rounded md:text-white hover:text-white hover:bg-transparent"
              style="border: 2px solid #fff;"
              aria-current="page"
              >{{ item.name }}</a
            >
            <a
              v-else
              @click="fn_getName"
              :href="item.name_path"
              class="topic_text_TH nav_item block z-0 py-2 px-1 text-white rounded hover:bg-gray-100 hover:bg-transparent "
              >{{ item.name }}</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
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
  font-size: 1.37rem;
  display: flex;
  justify-content: center;
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
