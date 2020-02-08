<template>
  <div
    id="app"
    class="container mx-auto px-32 bg-black text-white font-mono text-white"
  >
    <Header />
    <nuxt class="mb-4" />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  },
  methods: {
    toggleBodyClass(addRemoveClass, className) {
      const el = document.body

      if (addRemoveClass === 'addClass') {
        el.classList.add(className)
      } else {
        el.classList.remove(className)
      }
    }
  },
  mounted() {
    this.toggleBodyClass('addClass', 'bg-black')
  },
  destroyed() {
    this.toggleBodyClass('removeClass', 'bg-black')
  }
}
</script>
