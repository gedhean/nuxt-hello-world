<template>
  <div class="create">
    <h1>Create Page</h1>
  </div>
</template>

<script>
export default {
  head() {
    return {
      titleTemplate: '%s - Create Event',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Create awesome stuff with Nuxt.js!'
        }
      ]
    }
  }
}
</script>
