<template>
  <nav class="py-5 px-2 bg-black">
    <div
      class="max-w-screen flex flex-wrap items-center justify-between pl-12 pr-12"
    >
      <a href="#" class="flex items-center space-x-3 rtl:space-x-reverse">
        <span
          class="sty_logo self-center text-2xl font-semibold whitespace-nowrap text-white hover:text-orange-500"
          >Gavyn Miles</span
        >
      </a>
      <div class="hidden w-full md:block md:w-auto">
        <ul
          class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-black "
        >
          <li v-for="(item, index) in menubar" :key="index">
            <a
              v-if="index == 4"
              @click="fn_getName"
              href="/"
              class="topic_text_TH block z-1 py-1.5 px-4 text-white bg-orange-500 rounded md:text-white hover:text-white hover:bg-transparent"
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
.topic_text_TH {
  font-weight: 500;
  font-size: 23px;
}
.nav_item{
  cursor: pointer;
  position: relative;
}
.nav_item::before {
  content: " ";
  width: 2rem;
  height: 0.2rem;
  background: linear-gradient(90deg, #a993fe 0%, #f97316 100%);
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
