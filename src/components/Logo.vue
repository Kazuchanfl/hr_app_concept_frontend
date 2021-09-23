<template>
  <a id="Logo" href="#">Go All Out</a>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'Logo',
})
</script>

<style scoped>
a#Logo {
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 42px;
  display: flex;
  align-items: center;
  text-align: center;
  text-decoration: none;

  margin: 20px;

  color: #000000;
}

a#Logo:hover {
  color: #bfbfbf;
}
</style>