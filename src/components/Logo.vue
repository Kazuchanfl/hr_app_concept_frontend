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

@media screen and (min-width: 600px) {
  a#Logo {
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 42px;
    display: flex;
    align-items: center;
    text-align: center;
    text-decoration: none;

    width: 200px;

    margin: 20px;

    color: white;
  }

  a#Logo:hover {
    color: #dddddd;
  }
}

/* TODO takahashikazuaki define SP layout */
/* a#Logo {
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 42px;
  display: flex;
  align-items: center;
  text-align: center;
  text-decoration: none;

  width: 200px;

  margin: 20px;

  color: black;
}

a#Logo:hover {
  color: #dddddd;
} */
</style>