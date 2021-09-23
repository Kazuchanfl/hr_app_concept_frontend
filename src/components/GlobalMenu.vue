<template>
<div>
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

ul {
  padding-top: 1em;
  list-style: none;
}

a {
  font-size: 18px;
  display: flex;
  align-items: center;
  text-align: center;
  text-decoration: none;

  width: 150px;

  margin: 20px;

  color: #000000;
}

a:hover {
  color: #bfbfbf;
}
</style>