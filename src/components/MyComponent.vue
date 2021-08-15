<template>
  <h1>This is created by {{ accountName }}.</h1>

  <p>
    <a :href="githubLink + accountName" target="_blank">
      {{ accountName }}'s GitHub Profile
    </a>
  </p>

</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'MyComponent',
  props: {
    accountName: {
      type: String,
      required: true
    }
  },
  setup: () => {
      const githubLink = `https://github.com/`
      return { githubLink }
  }
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