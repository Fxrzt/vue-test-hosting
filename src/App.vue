<template>
  <div id="app">
    <NavbarMenu></NavbarMenu>
    <router-view/>
    <CopyRight></CopyRight>
  </div>
</template>

<script>
import NavbarMenu from './components/NavbarMenu.vue'
import CopyRight from './components/CopyRight.vue'

export default {
  components: {
    NavbarMenu,
    CopyRight
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

@import url('https://fonts.googleapis.com/css2?family=Lemon&display=swap');
.sty_logo{
  font-family: 'Lemon', serif;
  font-size: 30px;
  font-weight: 500;
}
.describ_text_EN{
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
}

@import url('https://fonts.googleapis.com/css2?family=K2D:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
/* .describ_text_TH{
  font-family: 'K2D', sans-serif;
} */
@import url('https://fonts.googleapis.com/css2?family=Barlow+Semi+Condensed:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
.describ_text_TH{
  font-family: 'Barlow Semi Condensed', sans-serif;
}

</style>
