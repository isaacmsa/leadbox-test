<template>
  <div>
    <header>
      <navbar />
    </header>
    <main>
      <slider :type="'banner'" :images="images" />
      <container :customClass="'bg-[#F2F2F2]'">
        <template #container>
          <featured-vehicles />
        </template>
      </container>
      <container :customClass="'bg-white'">
        <template #container>
          <details-vehicles />
        </template>
      </container>
      <container :customClass="'bg-[#219653]'">
        <template #container>
          <about-us />
        </template>
      </container>
    </main>
    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script>
import Container from './layout/Container.vue'
import Slider from './components/Slider.vue'
import Navbar from './layout/Navbar.vue'
import FeaturedVehicles from './views/FeaturedVehicles.vue'
import DetailsVehicles from './views/DetailsVehicles.vue'
import AboutUs from './views/AboutUs.vue'
import Footer from './layout/Footer.vue'

export default {
  components: {
    Container,
    Navbar,
    Slider,
    FeaturedVehicles,
    DetailsVehicles,
    AboutUs,
    Footer,
  },
  data() {
    return {
      images: [
        { id: 1, src: '/assets/images/ford-home-1.png', name: 'ford-home' },
        { id: 2, src: '/assets/images/tesla-home.png', name: 'tesla-home' },
      ],
    }
  },
}
</script>

<style></style>
