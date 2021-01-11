<template>
  <section class="banner-block" :id="'banner-block-'+id">
  <swiper ref="banner-slide" :options="settings">
    <swiper-slide v-for="banner in listBanner">
      <div class="single-slider content-v-center">
        <img src="" alt="">
      </div>
    </swiper-slide>
  </swiper>
  </section>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'

export default {
  name: 'banner',
  props: ['id'],
  components: {
    Swiper,
    SwiperSlide
  },
  directives: {
    swiper: directive
  },
  data() {
    return {
      settings: {
        loop: true,
        slidesPerView: 1,
        spaceBetween: 20
        // Some Swiper option/callback...
      }
    }
  },
  async fetch() {
    this.listPost = await this.$axios.$get('/api/post/related/' + this.id)
  }
}
</script>

<style scoped>

</style>
