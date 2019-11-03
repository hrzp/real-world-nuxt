<template>
  <h1>User: {{ username }}</h1>
</template>


<script>
export default {
  head() {
    return {
      titleTemplate: this.username,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.username + ' page'
        }
      ]
    }
  },
  computed: {
    username() {
      return this.$route.params.username
    }
  }
}
</script>


<style>
</style>