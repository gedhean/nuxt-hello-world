<template>
  <div class="event">
    <h1>Events</h1>

    <event-card v-for="(event, idx) in events" :key="idx" :event="event" />
  </div>
</template>

<script>
import EventCard from '~/components/EventCard.vue'

export default {
  components: {
    EventCard
  },

  asyncData({ $axios, error }) {
    return $axios
      .get('http://localhost:3030/events')
      .then(({ data }) => {
        return {
          events: data
        }
      })
      .catch((err) => {
        error({
          statusCode: 503,
          message: 'Unable to fetch events at this time, please try again' + err
        })
      })
  }
}
</script>
