<template>
  <div class="event">
    <h1>Event #{{ id }}</h1>
  </div>
</template>

<script>
export default {
  computed: {
    id() {
      return this.$route.params.id
    }
  },

  head() {
    return {
      titleTemplate: '%s - Create Event #' + this.id,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'What you need to know about event #' + this.id
        }
      ]
    }
  }
}
</script>
