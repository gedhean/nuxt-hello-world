<template>
  <div class="index">
    Hello World Nuxt.js
  </div>
</template>

<script>
export default {
  head() {
    return {
      titleTemplate: '%s - by Gêdhean',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Learning Nuxt.js by practicing.'
        }
      ]
    }
  }
}
</script>
