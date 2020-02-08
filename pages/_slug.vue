<template>
  <div>
    <h3 class="my-4">> {{ slug }}</h3>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: 'Richard Bagshaw - About Me',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'About Me | Richard Bagshaw Freelance Web Developer'
        }
      ]
    }
  },
  computed: {
    slug() {
      return this.$route.params.slug
    }
  }
}
</script>
