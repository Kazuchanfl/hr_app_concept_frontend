<template>
  <ul>
    <li class="logo"><Logo></Logo></li>
    <li><p>Home</p></li>
    <li><p>Mission & Values</p></li>
    <li><p>Goals</p></li>
    <li><p>Activities</p></li>
    <li><p>Feedbacks</p></li>
    <li><p>Explore</p></li>
    <li><p>Settings</p></li>
  </ul>
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
    list-style: none;
}

p {
  font-size: 18px;
  display: flex;
  align-items: center;
  text-align: center;

  margin: 20px;

  color: #000000;
}
</style>