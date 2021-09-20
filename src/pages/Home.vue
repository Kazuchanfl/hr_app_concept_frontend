<template>
  <GlobalMenu></GlobalMenu>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import GlobalMenu from '../components/GlobalMenu.vue'

export default defineComponent({
  components: { GlobalMenu },
  name: 'Home',
  props: {
    accountName: {
      type: String,
      required: true
    }
  },
  setup: () => {
      const githubLink = `https://github.com/`
      return { githubLink }
  },
})
</script>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>