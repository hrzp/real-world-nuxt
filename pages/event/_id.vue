<template>
  <h1>{{ event.title }}</h1>
</template>


<script>
export default {
  head() {
    return {
      titleTemplate: 'Event: ' + this.event.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'What you need to know about event:' + this.event.title
        }
      ]
    }
  },
  async asyncData({ $axios, error, params }) {
    try {
      const { data } = await $axios.get(
        'http://localhost:3030/events/' + params.id
      )
      return {
        event: data
      }
    } catch (e) {
      error({
        statusCode: 503,
        message: 'Unabel to fetch event #' + params.id
      })
    }
  }
}
</script>


<style>
</style>