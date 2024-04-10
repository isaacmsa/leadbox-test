<template>
  <div class="pt-14 lg:pt-16 pb-10 lg:pb-24 px-9">
    <Title
      :styles="'text-center uppercase mb-8 md:mb-14'"
      :title="'featured vehicles'"
    />
    <slider :isResponsive="true" :type="'small'" :images="images" />
  </div>
</template>

<script>
import Slider from '../components/Slider.vue'
import Title from '../components/Title.vue'

export default {
  components: { Title, Slider },
  data() {
    return {
      images: [
        { id: 1, src: '/assets/images/tesla-home.png', name: 'tesla-home-1' },
        { id: 2, src: '/assets/images/tesla-home.png', name: 'tesla-home-2' },
        { id: 3, src: '/assets/images/tesla-home.png', name: 'tesla-home-3' },
        { id: 4, src: '/assets/images/tesla-home.png', name: 'tesla-home-1' },
        { id: 5, src: '/assets/images/tesla-home.png', name: 'tesla-home-2' },
        { id: 6, src: '/assets/images/tesla-home.png', name: 'tesla-home-3' },
      ],
    }
  },
}
</script>

<style></style>
