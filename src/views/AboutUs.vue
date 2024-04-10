<template>
  <div class="relative">
    <div class="image-background"></div>
    <div
      class="absolute right-0 top-11 md:top-0 opacity-80 bg-[#219653] pt-8 md:pt-0.5 lg:pt-8 px-8 md:px-6 lg:px-8 pb-8 md:pb-1 lg:pb-8 md:w-7/12 lg:w-8/12"
    >
      <Title
        :styles="'text-center uppercase text-white mb-5'"
        :title="'about us'"
      />

      <sub-title
        :styleContainer="'mb-3'"
        :styleText="'font-normal text-xs text-white'"
        :subTitle="'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum vel quam nec metus pellentesque iaculis. Cras lobortis odio a nulla condimentum blandit. Donec laoreet euismod diam, in lobortis odio tincidunt in.'"
      />
      <sub-title
        :styleText="'font-normal text-xs text-white'"
        :subTitle="'Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Vivamus eleifend, metus ut rutrum dignissim, erat diam pulvinar urna, laoreet convallis odio lorem at elit. Morbi iaculis metus et vestibulum commodo. Duis dictum condimentum viverra. Curabitur cursus,'"
      />
    </div>
    <figure class="absolute bottom-0 md:top-10">
      <img
        class="md:w-80 lg:w-3/4 xl:w-3/4"
        src="/assets/images/about-persons-merge.png"
        alt=""
      />
    </figure>
  </div>
</template>

<script>
import SubTitle from '../components/SubTitle.vue'
import Title from '../components/Title.vue'
export default {
  components: { Title, SubTitle },
}
</script>

<style>
.image-background {
  background-image: url('/assets/images/about-mobile.png');
  opacity: 0.7;
  background-color: rgba(33, 150, 83, 0.7);
  height: 580px;
  padding-top: 42px;
}

@media (min-width: 768px) {
  .image-background {
    background-image: url('/assets/images/about-tablet.png');
    opacity: 0.7;
    background-color: rgba(33, 150, 83, 0.7);
    height: 305px;
    padding-top: 42px;
  }
}

@media (min-width: 1024px) {
  .image-background {
    background-image: url('/assets/images/about-background.png');
    opacity: 0.7;
    background-color: rgba(33, 150, 83, 0.7);
    height: 255px;
  }
}

@media (min-width: 1240px) {
  .image-background {
    background-image: url('/assets/images/about-background.png');
    opacity: 0.7;
    background-color: rgba(33, 150, 83, 0.7);
    height: 230px;
  }
}
</style>
