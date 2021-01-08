<template>
  <div class="container">
    <NuxtLink to="/sdf-dfsdf-p35">Test</NuxtLink>
  </div>
</template>

<script>
// import axios from 'axios'
export default {
  data() {
    return {
      info : {},
      modules : null
    }
  },
  head() {
    return {
      title : this.info.meta_title,
      meta : [
        {
          hid: 'description',
          name: 'description',
          content:
            this.info.meta_description
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: this.info.meta_key
        }
      ]
    }
  },
  mounted() {

  },
  asyncData({$axios}){
    return $axios.get('/api/homepage').then(response => {
      return {
        info : response.data[0]
      }
    })
  }
}
</script>
