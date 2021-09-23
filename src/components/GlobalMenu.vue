<template>
<div class="menu-background">
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
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Logo from './Logo.vue'
export default defineComponent({
  components: { Logo },
  name: 'GlobalMenu',
})
</script>
<style scoped>
*{box-sizing: border-box;}

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

ul {
  padding-top: 1em;
  list-style: none;
}

li {
  margin-top: 40px;
  margin-bottom: 40px;
}

a {
  font-size: 18px;
  display: flex;
  align-items: center;
  text-align: center;
  text-decoration: none;

  width: 150px;

  margin: 20px;

  color: white;
}

a:hover {
  color: #dddddd;
}
</style>