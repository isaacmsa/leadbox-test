<template>
  <carousel :breakpoints="breakpoints">
    <slide v-for="slide in images" :key="slide">
      <img
        v-if="type === 'banner'"
        :src="slide.src"
        :alt="slide.name"
        class="w-full h-60 md:h-96 lg:h-screen"
      />
      <card-sold :image="slide" v-else />
    </slide>

    <template #addons>
      <navigation />
    </template>
  </carousel>
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

import CardSold from '../views/components/CardSold.vue'

export default {
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
    CardSold,
  },
  props: {
    images: {
      type: Array,
      default: () => [],
    },
    type: String,
    isResponsive: Boolean,
  },
  data() {
    return {
      breakpoints: {
        768: {
          itemsToShow: this.isResponsive ? 2 : 1,
          snapAlign: 'center',
        },
        1024: {
          itemsToShow: this.isResponsive ? 3 : 1,
          snapAlign: 'start',
        },
      },
    }
  },
}
</script>
