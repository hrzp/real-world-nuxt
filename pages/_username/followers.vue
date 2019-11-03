<template>
  <h1>{{username}} Followrs are: []</h1>
</template>


<script>
export default {
  head() {
    return {
      titleTemplate: this.username + ' Followers',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.username + 'Followers Page'
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