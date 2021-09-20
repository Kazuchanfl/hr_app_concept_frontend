<template>
  <CommonLayout></CommonLayout>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CommonLayout from '../layouts/CommonLayout.vue'

export default defineComponent({
  components: { CommonLayout },
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
</style>