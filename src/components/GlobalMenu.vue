<template>
<div class="menu-background" v-if="menuIsOpened">
  <ul>
    <li class="logo"><Logo></Logo></li>
    <li><a href="#">Home</a></li>
    <li><a href="#">Mission & Values</a></li>
    <li><a href="#">Goals</a></li>
    <li><a href="#">Activities</a></li>
    <li><a href="#">Feedbacks</a></li>
    <li><a href="#">Explore</a></li>
    <li><a href="#">Settings</a></li>
  </ul>
</div>
<HamburgerMenu v-on:click="toggleMenu" v-bind:is-opened="menuIsOpened"></HamburgerMenu>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue'
import Logo from './Logo.vue'
import HamburgerMenu from './HamburgerMenu.vue'

const state = reactive({
  menuIsOpened: false
})

export default defineComponent({
  components: { Logo, HamburgerMenu },
  name: 'GlobalMenu',
  methods: {
    toggleMenu: function() {
      state.menuIsOpened = !state.menuIsOpened
      console.log(state.menuIsOpened)
    },
  },
  setup() {
    return state
  }
})
</script>
<style scoped>
*{box-sizing: border-box;}

ul {
  padding-top: 1em;
  list-style: none;
}


li {
  margin-top: 40px;
  margin-bottom: 40px;
}

a {
  font-size: 1em;
  display: flex;
  align-items: center;
  text-align: center;
  text-decoration: none;

  width: 150px;

  margin: 20px;

  font-weight: bold;
  /* color: white; */

  transition: 0.5s ;
}

a:hover {
  color: #dddddd;
}

@media screen and (min-width: 600px) {
  div.menu-background {
    background: linear-gradient(#f19aff, #66f6ff);
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 300px;
    border-top-right-radius: 45px;
    border-bottom-right-radius: 45px;
  }

  div.menu-background::after {
    content: '';
    display: block;
    position: absolute;
    z-index: -1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    background: linear-gradient(#f19aff, #66f6ff);
    border-top-right-radius: 45px;
    border-bottom-right-radius: 45px;
    filter: blur(20px);

    transform: translateX(10px);
    mix-blend-mode: multiply;
  }

  ul {
    padding-top: 1em;
    list-style: none;
  }

  li {
    margin-top: 40px;
    margin-bottom: 40px;
  }

  a {
    font-size: 1em;
    display: flex;
    align-items: center;
    text-align: center;
    text-decoration: none;

    width: 150px;

    margin: 20px;

    font-weight: bold;
    color: white;

    transition: 0.5s ;
  }

  a:hover {
    color: #dddddd;
  }
}


</style>