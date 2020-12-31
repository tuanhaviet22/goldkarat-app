<template>
  <div class="wrapper bg--shaft">
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      menuData: null,
      footerData: null,
      data: []
    }
  },
  methods: {
    getData() {
      this.$axios.$get('/api/config').then(response => {
        this.$store.state.global = response.data
          
      })
    }
  },
  created() {
    this.getData()
  }
}

</script>

<style>

</style>
