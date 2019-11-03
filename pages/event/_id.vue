<template>
  <h1>Event: #{{ id }}</h1>
</template>


<script>
export default {
  head() {
    return {
      titleTemplate: 'Event #' + this.id,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'What you need to know about event #' + this.id
        }
      ]
    }
  },
  computed: {
    id() {
      return this.$route.params.id
    }
  }
}
</script>


<style>
</style>